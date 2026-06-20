<template>
  <section id="urban" class="py-12">
    <div class="max-w-[1280px] mx-auto px-6">

      <div class="flex items-center gap-4 mb-8 flex-wrap">
        <span class="text-[15px] font-semibold text-slate-600">در چه مرحله‌ای از ساخت هستید؟</span>
        <span class="flex-1 h-px bg-slate-200"></span>
        <span class="bg-teal-500 text-white font-extrabold text-sm px-6 py-2.5 rounded-full">ثبت درخواست‌ های شهرسازی</span>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-5">

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-[0_6px_24px_rgba(28,58,107,.06)] text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg class="w-[84px] h-[84px]" viewBox="0 0 84 84">
                <rect x="20" y="14" width="44" height="56" rx="6" fill="#e6f7f0" stroke="#27b783" stroke-width="2" />
                <path d="M28 26h28M28 36h28M28 46h18" stroke="#27b783" stroke-width="2.5" stroke-linecap="round" />
                <circle cx="62" cy="62" r="11" fill="#27b783" />
                <path d="M57 62l3.5 3.5L67 58" stroke="#fff" stroke-width="2.5" fill="none" stroke-linecap="round" stroke-linejoin="round" />
                <circle cx="18" cy="18" r="6" fill="#f6a73c" />
              </svg>
            </div>
          </template>
          <template #title>
            <span class="inline-flex items-center gap-2 text-emerald-500 text-lg font-extrabold border-b-[3px] border-current pb-2">
              <span class="w-[18px] h-[3px] rounded bg-current"></span>
              پیش از ساخت
            </span>
          </template>
          <template #content>
            <ul class="flex flex-col gap-2">
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-semibold text-slate-700 hover:bg-slate-100 transition">
                <span>صدور پروانه</span>
                <span class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-[#1c3a6b]"><use href="#i-file-plus" /></svg>
                </span>
              </li>
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-bold text-emerald-500">
                <span>توقف مجوز کسب و پیشه</span>
                <span class="w-8 h-8 rounded-lg bg-emerald-50 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-emerald-500"><use href="#i-alert" /></svg>
                </span>
              </li>
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-semibold text-slate-700 hover:bg-slate-100 transition">
                <span>دریافت مفاصا</span>
                <span class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-[#1c3a6b]"><use href="#i-doc" /></svg>
                </span>
              </li>
            </ul>
          </template>
        </Card>

       
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-[0_6px_24px_rgba(28,58,107,.06)] text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg class="w-[84px] h-[84px]" viewBox="0 0 84 84">
                <rect x="14" y="44" width="14" height="26" fill="#3a6fd8" />
                <rect x="32" y="34" width="14" height="36" fill="#1c3a6b" />
                <rect x="50" y="50" width="14" height="20" fill="#3a6fd8" />
                <line x1="14" y1="44" x2="14" y2="14" stroke="#1c3a6b" stroke-width="3" />
                <line x1="14" y1="14" x2="58" y2="24" stroke="#1c3a6b" stroke-width="3" />
                <line x1="14" y1="20" x2="40" y2="20" stroke="#1c3a6b" stroke-width="3" />
                <line x1="40" y1="20" x2="40" y2="34" stroke="#f6a73c" stroke-width="2.5" />
                <rect x="34" y="34" width="12" height="8" rx="1" fill="#f6a73c" />
              </svg>
            </div>
          </template>
          <template #title>
            <span class="inline-flex items-center gap-2 text-[#1c3a6b] text-lg font-extrabold border-b-[3px] border-current pb-2">
              <span class="w-[18px] h-[3px] rounded bg-current"></span>
              در حال ساخت
            </span>
          </template>
          <template #content>
            <ul class="flex flex-col gap-2">
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-semibold text-slate-700 hover:bg-slate-100 transition">
                <span>تمدید / تجدید پروانه</span>
                <span class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-[#1c3a6b]"><use href="#i-file-plus" /></svg>
                </span>
              </li>
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-semibold text-slate-700 hover:bg-slate-100 transition">
                <span>اصلاح پروانه</span>
                <span class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-[#1c3a6b]"><use href="#i-edit" /></svg>
                </span>
              </li>
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-semibold text-slate-700 hover:bg-slate-100 transition">
                <span>عدم خلاف</span>
                <span class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-[#1c3a6b]"><use href="#i-badge" /></svg>
                </span>
              </li>
            </ul>
          </template>
        </Card>

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-[0_6px_24px_rgba(28,58,107,.06)] text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg class="w-[84px] h-[84px]" viewBox="0 0 84 84">
                <rect x="22" y="18" width="40" height="50" rx="4" fill="#fff7ea" stroke="#f6a73c" stroke-width="2" />
                <line x1="30" y1="28" x2="30" y2="28.1" stroke="#f6a73c" stroke-width="4" stroke-linecap="round" />
                <line x1="42" y1="28" x2="42" y2="28.1" stroke="#f6a73c" stroke-width="4" stroke-linecap="round" />
                <line x1="54" y1="28" x2="54" y2="28.1" stroke="#f6a73c" stroke-width="4" stroke-linecap="round" />
                <line x1="30" y1="40" x2="30" y2="40.1" stroke="#f6a73c" stroke-width="4" stroke-linecap="round" />
                <line x1="42" y1="40" x2="42" y2="40.1" stroke="#f6a73c" stroke-width="4" stroke-linecap="round" />
                <line x1="54" y1="40" x2="54" y2="40.1" stroke="#f6a73c" stroke-width="4" stroke-linecap="round" />
                <circle cx="58" cy="58" r="12" fill="#f6a73c" />
                <path d="M52 58l4 4 8-8" stroke="#fff" stroke-width="2.5" fill="none" stroke-linecap="round" stroke-linejoin="round" />
              </svg>
            </div>
          </template>
          <template #title>
            <span class="inline-flex items-center gap-2 text-amber-500 text-lg font-extrabold border-b-[3px] border-current pb-2">
              <span class="w-[18px] h-[3px] rounded bg-current"></span>
              پس از ساخت
            </span>
          </template>
          <template #content>
            <ul class="flex flex-col gap-2">
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-semibold text-slate-700 hover:bg-slate-100 transition">
                <span>توسعه بنا / اضافه اشکوب</span>
                <span class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-[#1c3a6b]"><use href="#i-building" /></svg>
                </span>
              </li>
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-semibold text-slate-700 hover:bg-slate-100 transition">
                <span>پایان کار</span>
                <span class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-[#1c3a6b]"><use href="#i-badge" /></svg>
                </span>
              </li>
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-semibold text-slate-700 hover:bg-slate-100 transition">
                <span>تعلیق مجوز کسب و پیشه</span>
                <span class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-[#1c3a6b]"><use href="#i-alert" /></svg>
                </span>
              </li>
            </ul>
          </template>
        </Card>

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-[0_6px_24px_rgba(28,58,107,.06)] text-center">
          <template #header>
            <div class="flex justify-center pt-6">
              <svg class="w-[84px] h-[84px]" viewBox="0 0 84 84">
                <rect x="18" y="34" width="48" height="32" rx="5" fill="#eaf2ff" stroke="#1c3a6b" stroke-width="2" />
                <rect x="32" y="24" width="20" height="12" rx="3" fill="none" stroke="#1c3a6b" stroke-width="2.5" />
                <line x1="18" y1="46" x2="66" y2="46" stroke="#1c3a6b" stroke-width="2" />
                <rect x="36" y="42" width="12" height="9" rx="1.5" fill="#3a6fd8" />
                <circle cx="64" cy="60" r="3" fill="#27b783" />
              </svg>
            </div>
          </template>
          <template #title>
            <span class="inline-flex items-center gap-2 text-[#1c3a6b] text-lg font-extrabold border-b-[3px] border-current pb-2">
              <span class="w-[18px] h-[3px] rounded bg-current"></span>
              سایر درخواست‌ها
            </span>
          </template>
          <template #content>
            <ul class="flex flex-col gap-2">
              <li class="flex items-center justify-between gap-3 px-4 py-3 rounded-xl text-sm font-semibold text-slate-700 hover:bg-slate-100 transition">
                <span>استعلام</span>
                <span class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center shrink-0">
                  <svg class="w-4 h-4 text-[#1c3a6b]"><use href="#i-doc-search" /></svg>
                </span>
              </li>
            </ul>
          </template>
        </Card>

      </div>
    </div>
  </section>
</template>
