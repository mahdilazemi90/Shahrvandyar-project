<template>
  <section class="py-7">
    <div class="max-w-[1280px] mx-auto px-6 flex flex-col lg:flex-row gap-5">

      
      <div class="flex flex-col gap-4 w-full lg:w-[320px] shrink-0">

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-[0_6px_24px_rgba(28,58,107,.06)] flex-1 text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg width="64" height="64" viewBox="0 0 64 64">
                <rect x="18" y="6" width="28" height="50" rx="6" fill="#eaf2ff" stroke="#3a6fd8" stroke-width="2" />
                <rect x="23" y="13" width="18" height="28" rx="2" fill="#fff" />
                <circle cx="32" cy="48" r="2" fill="#3a6fd8" />
                <circle cx="46" cy="40" r="9" fill="#27b783" />
                <path d="M42 40l3 3 6-6" stroke="#fff" stroke-width="2.5" fill="none" stroke-linecap="round" stroke-linejoin="round" />
                <circle cx="14" cy="14" r="6" fill="#f6a73c" />
                <circle cx="14" cy="14" r="2.5" fill="#fff" />
              </svg>
            </div>
          </template>
          <template #title>
            <span class="text-lg font-extrabold text-[#1c3a6b]">پرداخت عوارض</span>
          </template>
          <template #content>
            <p class="text-xs text-slate-500 m-0">عوارض ساختمان خود را مشاهده کنید</p>
          </template>
        </Card>

       
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-[0_6px_24px_rgba(28,58,107,.06)] flex-1 text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg width="64" height="64" viewBox="0 0 64 64">
                <rect x="22" y="10" width="24" height="44" rx="5" fill="#eaf2ff" stroke="#3a6fd8" stroke-width="2" />
                <rect x="26" y="16" width="16" height="24" rx="2" fill="#fff" />
                <circle cx="34" cy="48" r="2" fill="#3a6fd8" />
                <rect x="29" y="22" width="10" height="8" rx="1.5" fill="#27b783" />
                <circle cx="34" cy="26" r="2.4" fill="#fff" />
                <path d="M10 50 24 36" stroke="#f6a73c" stroke-width="3" stroke-linecap="round" />
                <circle cx="10" cy="50" r="4" fill="#f6a73c" />
              </svg>
            </div>
          </template>
          <template #title>
            <span class="block text-[34px] font-extrabold text-emerald-500">۱۳۷</span>
            <span class="text-lg font-extrabold text-[#1c3a6b]">گزارش مردمی</span>
          </template>
          <template #content>
            <p class="text-xs text-slate-500 m-0">ثبت تخلفات ساختمانی و شهرسازی</p>
          </template>
        </Card>

      </div>

     
      <div class="flex-1 relative overflow-hidden rounded-[18px] min-h-[340px] bg-gradient-to-br from-[#15294f] via-[#2c5694] to-[#5891c9]">

        <svg class="w-full h-full" viewBox="0 0 800 400" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="sky" x1="0" y1="0" x2="0" y2="1">
              <stop offset="0" stop-color="#1b3a6b" />
              <stop offset="1" stop-color="#5d9bd6" />
            </linearGradient>
          </defs>
          <rect width="800" height="400" fill="url(#sky)" />
          <rect x="40" y="220" width="60" height="180" fill="#ffffff" opacity="0.08" />
          <rect x="120" y="180" width="50" height="220" fill="#ffffff" opacity="0.1" />
          <rect x="650" y="200" width="70" height="200" fill="#ffffff" opacity="0.08" />
          <rect x="730" y="160" width="50" height="240" fill="#ffffff" opacity="0.1" />
          <g opacity="0.95">
            <rect x="260" y="120" width="220" height="280" fill="#cfe0f4" opacity="0.9" />
          </g>
        </svg>

        <div class="absolute inset-0 flex flex-col justify-center items-end text-right px-12 max-lg:items-center max-lg:text-center max-lg:px-6">
          <h1 class="text-white text-4xl font-extrabold leading-[1.5] drop-shadow-lg">انجام فرآیندهای شهرسازی</h1>
          <h2 class="text-[#e6eefc] text-lg font-medium mt-2 mb-6">بدون مراجعه حضوری</h2>
          <Button
            as="a"
            href="#urban"
            label="ثبت درخواست شهرسازی"
            class="!bg-white !text-[#1c3a6b] !font-bold !text-[15px] !px-7 !py-3.5 !rounded-xl !border-0 !shadow-lg hover:!bg-teal-500 hover:!text-white"
          />
        </div>

      </div>

    </div>
  </section>
</template>
