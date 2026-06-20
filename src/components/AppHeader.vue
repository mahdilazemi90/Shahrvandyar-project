<template>
  <header class="bg-white border-b border-[var(--border)]">
    <div class="max-w-[1280px] mx-auto px-6 flex items-center gap-7 py-[18px]">

      
      <div class="flex flex-col items-end gap-0.5 shrink-0">
        <span class="text-[26px] font-extrabold bg-gradient-to-r from-[#3a6fd8] to-[#1cc6b6] bg-clip-text text-transparent tracking-[0.5px]">
          شهروندیار
        </span>
        <span class="text-[11px] text-[var(--muted)] font-medium">
          خدمتگزار هوشمند شهر
        </span>
      </div>

      
      

      <AuthDialog v-model:visible="authVisible" />

      
      <IconField class="flex-1">
        <InputIcon>
          <svg class="w-[18px] h-[18px] text-[var(--muted)] stroke-current fill-none [stroke-width:1.9] [stroke-linecap:round] [stroke-linejoin:round]">
            <use href="#i-search" />
          </svg>
        </InputIcon>
        <InputText
          v-model="query"
          placeholder="جستجو در سایت (صفحه، خدمت، عوارض...)"
          class="w-full !bg-[var(--bg)] !border !border-[var(--border)] !rounded-[10px] !text-[14px]"
        />
      </IconField>
      <Button
        text
        @click="authVisible = true"
        class="!px-5 !py-[11px] !border !border-[var(--border)] !rounded-[10px] !text-[14px] !font-semibold !text-[var(--navy)] whitespace-nowrap hover:!bg-[var(--teal-bg)] hover:!border-[var(--teal)]"
      >
        <span class="flex items-center gap-2">
          <svg class="w-[18px] h-[18px] shrink-0 text-[var(--teal-deep)] stroke-current fill-none [stroke-width:1.9] [stroke-linecap:round] [stroke-linejoin:round]">
            <use href="#i-user" />
          </svg>
          ورود / ثبت‌نام
        </span>
      </Button>

    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import AuthDialog from './AuthDialog.vue'

const query = ref('')
const authVisible = ref(false)
</script>
