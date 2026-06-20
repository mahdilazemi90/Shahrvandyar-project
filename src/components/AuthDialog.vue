<template>
  <Dialog
    v-model:visible="visible"
    modal
    :draggable="false"
    :style="{ width: '380px' }"
    header="ورود / ثبت‌نام"
    class="!rounded-2xl"
  >
    <Tabs v-model:value="activeTab">
      <TabList>
        <Tab value="login">ورود</Tab>
        <Tab value="register">ثبت‌نام</Tab>
      </TabList>

      <TabPanels>

        
        <TabPanel value="login">
          <form class="flex flex-col gap-4 pt-4" @submit.prevent="submitLogin">

            <div class="flex flex-col gap-1.5">
              <label class="text-sm font-semibold text-[var(--navy)]">ایمیل یا نام کاربری</label>
              <InputText v-model="login.identity" placeholder="ایمیل یا نام کاربری" class="w-full" />
            </div>

            <div class="flex flex-col gap-1.5">
              <label class="text-sm font-semibold text-[var(--navy)]">رمز عبور</label>
              <Password v-model="login.password" :feedback="false" toggleMask placeholder="رمز عبور" class="w-full" inputClass="w-full" />
            </div>

            <Message v-if="loginError" severity="error" :closable="false">{{ loginError }}</Message>

            <Button type="submit" label="ورود" class="w-full !mt-1" />
          </form>
        </TabPanel>

        
        <TabPanel value="register">
          <form class="flex flex-col gap-4 pt-4" @submit.prevent="submitRegister">

            <div class="flex flex-col gap-1.5">
              <label class="text-sm font-semibold text-[var(--navy)]">نام کاربری</label>
              <InputText v-model="register.username" placeholder="نام کاربری" class="w-full" />
            </div>

            <div class="flex flex-col gap-1.5">
              <label class="text-sm font-semibold text-[var(--navy)]">ایمیل</label>
              <InputText v-model="register.email" type="email" placeholder="ایمیل" class="w-full" />
            </div>

            <div class="flex flex-col gap-1.5">
              <label class="text-sm font-semibold text-[var(--navy)]">رمز عبور</label>
              <Password v-model="register.password" toggleMask placeholder="رمز عبور" class="w-full" inputClass="w-full" />
            </div>

            <div class="flex flex-col gap-1.5">
              <label class="text-sm font-semibold text-[var(--navy)]">تکرار رمز عبور</label>
              <Password v-model="register.confirm" :feedback="false" toggleMask placeholder="تکرار رمز عبور" class="w-full" inputClass="w-full" />
            </div>

            <Message v-if="registerError" severity="error" :closable="false">{{ registerError }}</Message>
            <Message v-if="registerSuccess" severity="success" :closable="false">{{ registerSuccess }}</Message>

            <Button type="submit" label="ثبت‌نام" class="w-full !mt-1" />
          </form>
        </TabPanel>

      </TabPanels>
    </Tabs>
  </Dialog>
</template>

<script setup>
import { ref } from 'vue'

// v-model:visible from the parent (e.g. <AuthDialog v-model:visible="authVisible" />)
const visible = defineModel('visible', { default: false })

const activeTab = ref('login')

/* ---------------- ورود ---------------- */
const login = ref({ identity: '', password: '' })
const loginError = ref('')

function submitLogin() {
  loginError.value = ''

  if (!login.value.identity || !login.value.password) {
    loginError.value = 'لطفاً ایمیل/نام کاربری و رمز عبور را وارد کنید.'
    return
  }

  // TODO: این بخش را به فراخوانی API واقعی متصل کنید
  console.log('login payload:', login.value)
  visible.value = false
}

/* ---------------- ثبت‌نام ---------------- */
const register = ref({ username: '', email: '', password: '', confirm: '' })
const registerError = ref('')
const registerSuccess = ref('')

function submitRegister() {
  registerError.value = ''
  registerSuccess.value = ''

  const r = register.value

  if (!r.username || !r.email || !r.password || !r.confirm) {
    registerError.value = 'لطفاً همه‌ی فیلدها را پر کنید.'
    return
  }
  if (!/^\S+@\S+\.\S+$/.test(r.email)) {
    registerError.value = 'ایمیل وارد شده معتبر نیست.'
    return
  }
  if (r.password.length < 6) {
    registerError.value = 'رمز عبور باید حداقل ۶ کاراکتر باشد.'
    return
  }
  if (r.password !== r.confirm) {
    registerError.value = 'رمز عبور و تکرار آن یکسان نیستند.'
    return
  }

  
  console.log('register payload:', r)
  registerSuccess.value = 'ثبت‌نام با موفقیت انجام شد!'
}
</script>
