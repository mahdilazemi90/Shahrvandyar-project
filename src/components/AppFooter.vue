<template>
  <footer class="bg-[var(--navy-deep)] text-[#cdd9ee] mt-10">
    <div class="max-w-[1280px] mx-auto px-6 flex flex-wrap gap-10 py-12 pb-8">

      <div class="flex-1 min-w-[220px]">
        <div class="text-[30px] font-extrabold bg-gradient-to-r from-[#6fa8ff] to-[#1cc6b6] bg-clip-text text-transparent">
          شهروندیار
        </div>
        <div class="text-[13px] text-[#7e91ba] mt-1.5">خدمتگزار هوشمند شهر</div>
      </div>

      <div class="flex-1 min-w-[200px]">
        <h4 class="text-white text-[16px] font-extrabold mb-5">خدمات سامانه</h4>
        <ul>
          <li v-for="item in services" :key="item.label" class="flex items-center gap-2.5 text-[13.5px] text-[#a9bbdc] py-[7px]">
            <svg class="w-4 h-4 text-[var(--teal)]"><use :href="`#${item.icon}`" /></svg>
            {{ item.label }}
          </li>
        </ul>
      </div>

      <div class="flex-1 min-w-[200px]">
        <h4 class="text-white text-[16px] font-extrabold mb-5">لینک‌های مفید</h4>
        <ul>
          <li v-for="link in links" :key="link" class="flex items-center gap-2.5 text-[13.5px] text-[#a9bbdc] py-[7px]">
            <span class="w-1.5 h-1.5 rounded-full bg-[var(--teal)] shrink-0"></span>
            {{ link }}
          </li>
        </ul>
      </div>

      <div class="flex-1 min-w-[200px]">
        <h4 class="text-white text-[16px] font-extrabold mb-5">تماس با ما</h4>
        <ul>
          <li v-for="item in contact" :key="item.label" class="flex items-center gap-2.5 text-[13.5px] text-[#a9bbdc] py-[7px]">
            <svg class="w-4 h-4 text-[var(--teal)]"><use :href="`#${item.icon}`" /></svg>
            {{ item.label }}
          </li>
        </ul>
      </div>

    </div>

    <div class="border-t border-white/10 py-[18px] text-center text-[12.5px] text-[#7e91ba]">
      © ۱۴۰۵ شهروندیار — کلیه حقوق محفوظ است
    </div>
  </footer>
</template>

<script setup>
const services = [
  { label: 'نقشه', icon: 'i-map' },
  { label: 'ثبت درخواست‌های شهرسازی', icon: 'i-file-plus' },
  { label: 'پرداخت عوارض', icon: 'i-card' },
  { label: 'گزارش مردمی', icon: 'i-alert' },
  { label: 'تصدیق گواهی', icon: 'i-badge' },
  { label: 'خوداظهاری', icon: 'i-edit' },
  { label: 'کیف ملک', icon: 'i-house' },
  { label: 'پیام‌ها و ابلاغیه‌ها', icon: 'i-mail' }
]

const links = [
  'سازمان مناطق آزاد ایران',
  'منطقه آزاد چابهار',
  'شورای عالی مناطق آزاد',
  'پایگاه خبری مناطق آزاد',
  'سازمان سرمایه‌گذاری و کمک‌های اقتصادی و فنی'
]

const contact = [
  { label: '۰۵۴۳۵۳۱۲۲۰۰', icon: 'i-phone' },
  { label: '۳۰۰۰۵۰۱۵', icon: 'i-phone' },
  { label: '۰۵۴۳۵۳۱۲۲۲۹', icon: 'i-phone' },
  { label: 'info@cfzo.ir', icon: 'i-mail' },
  { label: 'شورای عالی مناطق آزاد', icon: 'i-pin' },
  { label: 'شناسه ملی سازمان: ۱۰۱۰۰۴۰۴۲۰۰', icon: 'i-id' }
]
</script>
