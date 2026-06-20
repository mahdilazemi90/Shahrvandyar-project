<template>
  <section class="py-[46px]">
    <div class="max-w-[1280px] mx-auto px-6">

      <div class="flex items-center justify-center gap-[18px] mb-[30px]">
        <span class="flex-1 h-px bg-[var(--border)]"></span>
        <span class="bg-[var(--green)] text-white font-extrabold text-[14px] py-[10px] px-[22px] rounded-full whitespace-nowrap">سوالات متداول</span>
        <span class="flex-1 h-px bg-[var(--border)]"></span>
      </div>

      
      <Accordion value="0" class="max-w-[980px] mx-auto flex flex-col gap-[14px]">
        <AccordionPanel
          v-for="(faq, i) in faqs"
          :key="faq.q"
          :value="String(i)"
          class="!bg-white !border !border-[var(--border)] !rounded-[14px] overflow-hidden !shadow-[var(--shadow)]"
        >
          <AccordionHeader class="!text-[15px] !font-bold !text-[var(--navy)]">{{ faq.q }}</AccordionHeader>
          <AccordionContent>
            <p class="text-[13.5px] text-[#5a6c8c] max-w-[90ch] m-0">{{ faq.a }}</p>
          </AccordionContent>
        </AccordionPanel>
      </Accordion>

      <div class="flex justify-center mt-6">
        <Button
          label="مشاهده بیشتر"
          text
          class="!bg-[var(--teal-bg)] !text-[var(--teal-deep)] !font-bold !text-[14px] !px-8 !py-3 !rounded-[10px] hover:!bg-[var(--teal)] hover:!text-white"
        >
          <template #icon>
            <svg class="w-[15px] h-[15px]"><use href="#i-chevron" /></svg>
          </template>
        </Button>
      </div>

    </div>
  </section>
</template>

<script setup>
const faqs = [
  {
    q: 'سامانه شهروندیار چیست؟',
    a: 'شهروندیار، درگاه خدمات هوشمند و یکپارچه مدیریت شهری است که تمامی خدمات شهرداری اعم از شهرسازی، پرداخت عوارض، ثبت گزارش‌های مردمی (مانند سامانه ۱۳۷) و استعلامات را به‌صورت آنلاین و بدون نیاز به مراجعه حضوری به شهروندان ارائه می‌دهد.'
  },
  {
    q: 'آیا برای استفاده از خدمات سامانه حتماً باید ثبت‌نام کنم؟',
    a: 'برای مشاهده اطلاعات عمومی سامانه نیازی به ثبت‌نام نیست، اما برای ثبت درخواست، پرداخت عوارض و پیگیری پرونده باید با کد ملی و شماره موبایل خود ثبت‌نام و احراز هویت کنید.'
  },
  {
    q: 'چگونه از تسویه شدن عوارض خود مطمئن شوم؟',
    a: 'پس از هر پرداخت، یک رسید الکترونیکی همراه با کد رهگیری صادر می‌شود. کافی است از بخش «رهگیری فیش» با وارد کردن کد رهگیری یا شماره پرونده، وضعیت تسویه را بررسی کنید.'
  },
  {
    q: 'برای شروع ساخت‌وساز در یک زمین خالی با کلنگی چه درخواستی ثبت کنم؟',
    a: 'برای زمین خالی یا ملک کلنگی باید از بخش «پیش از ساخت» گزینه «صدور پروانه» را انتخاب و مدارک مالکیت، نقشه ملک و سایر اسناد لازم را بارگذاری کنید تا پرونده شما بررسی شود.'
  }
]
</script>
