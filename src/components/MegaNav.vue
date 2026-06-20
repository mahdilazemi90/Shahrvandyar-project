<template>
  <div class="relative bg-[var(--navy)]" ref="navWrap" @mouseleave="hide">
    <nav class="max-w-[1280px] mx-auto px-6 flex items-stretch">

      <a href="#" class="flex items-center gap-2 px-[22px] py-[15px] text-[14.5px] font-medium text-[#dbe6f7] border-l border-white/5 whitespace-nowrap transition hover:bg-white/5 hover:text-white">
        <svg class="w-[17px] h-[17px] stroke-current fill-none [stroke-width:1.9] [stroke-linecap:round] [stroke-linejoin:round]"><use href="#i-map" /></svg>
        نقشه
      </a>

      
      <button
        type="button"
        @click="toggle"
        @mouseenter="show"
        class="flex items-center gap-2 px-[22px] py-[15px] text-[14.5px] font-medium bg-white text-[var(--navy)] rounded-b-[12px] whitespace-nowrap"
      >
        <svg class="w-[17px] h-[17px] stroke-current fill-none [stroke-width:1.9] [stroke-linecap:round] [stroke-linejoin:round]"><use href="#i-file-plus" /></svg>
        ثبت درخواست
        <svg class="mr-auto w-[13px] h-[13px] stroke-current fill-none [stroke-width:1.9] [stroke-linecap:round] [stroke-linejoin:round]"><use href="#i-chevron" /></svg>
      </button>

      <a href="#" class="flex items-center gap-2 px-[22px] py-[15px] text-[14.5px] font-medium text-[#dbe6f7] border-l border-white/5 whitespace-nowrap transition hover:bg-white/5 hover:text-white">
        <svg class="w-[17px] h-[17px] stroke-current fill-none [stroke-width:1.9] [stroke-linecap:round] [stroke-linejoin:round]"><use href="#i-card" /></svg>
        پرداخت عوارض
      </a>

      <a href="#" class="flex items-center gap-2 px-[22px] py-[15px] text-[14.5px] font-medium text-[#dbe6f7] border-l border-white/5 whitespace-nowrap transition hover:bg-white/5 hover:text-white">
        <svg class="w-[17px] h-[17px] stroke-current fill-none [stroke-width:1.9] [stroke-linecap:round] [stroke-linejoin:round]"><use href="#i-badge" /></svg>
        تصدیق گواهی
      </a>

      <a href="#" class="flex items-center gap-2 px-[22px] py-[15px] text-[14.5px] font-medium text-[#dbe6f7] border-l border-white/5 whitespace-nowrap transition hover:bg-white/5 hover:text-white">
        <svg class="w-[17px] h-[17px] stroke-current fill-none [stroke-width:1.9] [stroke-linecap:round] [stroke-linejoin:round]"><use href="#i-edit" /></svg>
        خوداظهاری
      </a>

      <a href="#" class="flex items-center gap-2 px-[22px] py-[15px] text-[14.5px] font-medium text-[#ffd27a] border-l border-white/5 whitespace-nowrap transition hover:bg-white/5">
        <svg class="w-[17px] h-[17px] text-[#ffb84d] stroke-current fill-none [stroke-width:1.9] [stroke-linecap:round] [stroke-linejoin:round]"><use href="#i-alert" /></svg>
        گزارش مردمی
      </a>

    </nav>

    
    <Popover
      ref="mega"
      class="!w-full !max-w-none !rounded-t-none !rounded-b-2xl !shadow-[0_16px_40px_rgba(20,40,80,.14)] !border-0 !mt-0"
      :pt="{ content: { class: '!p-7' } }"
    >
      <div class="flex gap-5 max-w-[1280px] mx-auto flex-wrap lg:flex-nowrap">
        <div v-for="group in groups" :key="group.title" class="flex-1 min-w-0">
          <div class="flex items-center justify-between gap-2 px-4 py-2.5 rounded-lg mb-2.5 text-white text-sm font-bold" :class="group.color">
            <span>{{ group.title }}</span>
            <svg class="w-3 h-3 text-white"><use href="#i-chevron" /></svg>
          </div>

          <ul>
            <li
              v-for="row in group.items"
              :key="row.label"
              class="flex items-center justify-between gap-2 px-4 py-2 text-[13px] rounded-lg transition"
              :class="row.active ? 'text-emerald-500 font-bold' : 'text-slate-600 hover:bg-slate-100 hover:text-slate-800'"
            >
              <span>{{ row.label }}</span>
              <span v-if="row.active" class="text-[8px]">●</span>
              <svg v-else class="w-4 h-4 text-slate-400"><use :href="`#${row.icon}`" /></svg>
            </li>
          </ul>
        </div>
      </div>
    </Popover>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const mega = ref()
const navWrap = ref()

function toggle(e) {
  mega.value.toggle(e)
}
function show(e) {
  mega.value.show(e)
}
function hide() {
  mega.value.hide()
}

const groups = [
  {
    title: 'پیش از ساخت',
    color: 'bg-emerald-500',
    items: [
      { label: 'صدور پروانه', icon: 'i-file-plus' },
      { label: 'توقف مجوز کسب و پیشه', active: true },
      { label: 'دریافت مفاصا', icon: 'i-doc' }
    ]
  },
  {
    title: 'در حال ساخت',
    color: 'bg-[#1c3a6b]',
    items: [
      { label: 'تمدید / تجدید پروانه', icon: 'i-file-plus' },
      { label: 'اصلاح پروانه', icon: 'i-edit' },
      { label: 'عدم خلاف', icon: 'i-badge' }
    ]
  },
  {
    title: 'پس از ساخت',
    color: 'bg-amber-400',
    items: [
      { label: 'توسعه بنا / اضافه اشکوب', icon: 'i-building' },
      { label: 'پایان کار', icon: 'i-badge' },
      { label: 'تعلیق مجوز کسب و پیشه', icon: 'i-alert' }
    ]
  },
  {
    title: 'سایر درخواست‌ها',
    color: 'bg-sky-500',
    items: [
      { label: 'استعلام دفتر خانه', icon: 'i-search' },
      { label: 'استعلام بانک', icon: 'i-search' },
      { label: 'اداره برق', icon: 'i-search' },
      { label: 'دادگستری', icon: 'i-search' }
    ]
  }
]
</script>
