<template>
  <section class="py-12">
    <div class="max-w-[1280px] mx-auto px-6">

      <div class="flex items-center gap-4 mb-8 flex-wrap">
        <span class="text-[15px] font-semibold text-slate-600">عوارض ساختمان و کسب‌وکار خود را آنلاین مدیریت کنید</span>
        <span class="flex-1 h-px bg-slate-200"></span>
        <span class="bg-teal-500 text-white font-extrabold text-sm px-6 py-2.5 rounded-full">پرداخت عوارض</span>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-5">

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-lg text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg class="w-16 h-16" viewBox="0 0 64 64">
                <path d="M10 28 28 14l18 14" fill="none" stroke="#e8633f" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" />
                <rect x="14" y="28" width="28" height="22" fill="#fdeee9" stroke="#e8633f" stroke-width="2" />
                <rect x="24" y="36" width="8" height="14" fill="#fff" />
                <circle cx="44" cy="42" r="10" fill="#f6a73c" />
                <text x="44" y="46" font-size="11" font-weight="700" fill="#fff" text-anchor="middle">﷼</text>
              </svg>
            </div>
          </template>
          <template #title>
            <span class="text-lg font-extrabold text-[#1c3a6b]">عوارض نوسازی</span>
          </template>
          <template #content>
            <p class="text-sm text-slate-500 m-0">پرداخت عوارض نوسازی ساختمان</p>
          </template>
        </Card>

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-lg text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg class="w-16 h-16" viewBox="0 0 64 64">
                <rect x="16" y="10" width="28" height="38" rx="3" fill="#eafaf3" stroke="#27b783" stroke-width="2" />
                <line x1="22" y1="20" x2="38" y2="20" stroke="#27b783" stroke-width="2" />
                <line x1="22" y1="27" x2="38" y2="27" stroke="#27b783" stroke-width="2" />
                <line x1="22" y1="34" x2="32" y2="34" stroke="#27b783" stroke-width="2" />
                <circle cx="46" cy="44" r="11" fill="#27b783" />
                <text x="46" y="48" font-size="12" font-weight="700" fill="#fff" text-anchor="middle">﷼</text>
              </svg>
            </div>
          </template>
          <template #title>
            <span class="text-lg font-extrabold text-[#1c3a6b]">عوارض درآمدی</span>
          </template>
          <template #content>
            <p class="text-sm text-slate-500 m-0">پرداخت عوارض درآمدی</p>
          </template>
        </Card>

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-lg text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg class="w-16 h-16" viewBox="0 0 64 64">
                <path d="M8 24 11 12h42l3 12" fill="none" stroke="#f6a73c" stroke-width="2.5" stroke-linejoin="round" />
                <path d="M8 24a5 5 0 0 0 10 0 5 5 0 0 0 10 0 5 5 0 0 0 10 0 5 5 0 0 0 10 0" fill="none" stroke="#f6a73c" stroke-width="2.2" />
                <rect x="13" y="24" width="38" height="28" fill="#fff7ea" stroke="#f6a73c" stroke-width="2" />
                <rect x="27" y="38" width="10" height="14" fill="#fff" />
              </svg>
            </div>
          </template>
          <template #title>
            <span class="text-lg font-extrabold text-[#1c3a6b]">عوارض کسب و پیشه</span>
          </template>
          <template #content>
            <p class="text-sm text-slate-500 m-0">پرداخت عوارض کسب و کار و مشاغل</p>
          </template>
        </Card>

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-lg text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg class="w-16 h-16" viewBox="0 0 64 64">
                <path d="M16 8v44l4-2 4 2 4-2 4 2 4-2 4 2V8l-4 2-4-2-4 2-4-2-4 2z" fill="#eaf2ff" stroke="#3a6fd8" stroke-width="2" />
                <line x1="22" y1="18" x2="38" y2="18" stroke="#3a6fd8" stroke-width="2" />
                <line x1="22" y1="25" x2="38" y2="25" stroke="#3a6fd8" stroke-width="2" />
                <circle cx="46" cy="42" r="9" fill="none" stroke="#27b783" stroke-width="2.5" />
                <line x1="52.5" y1="48.5" x2="58" y2="54" stroke="#27b783" stroke-width="2.5" stroke-linecap="round" />
              </svg>
            </div>
          </template>
          <template #title>
            <span class="text-lg font-extrabold text-[#1c3a6b]">رهگیری فیش</span>
          </template>
          <template #content>
            <p class="text-sm text-slate-500 m-0">رهگیری فیش‌های عوارض</p>
          </template>
        </Card>

      </div>
    </div>
  </section>
</template>
