<template>
  <section class="py-12">
    <div class="max-w-[1280px] mx-auto px-6">

      <div class="flex items-center gap-4 mb-8 flex-wrap">
        <span class="text-[15px] font-semibold text-slate-600">صاحب کسب و کار و کار هستید؟</span>
        <span class="flex-1 h-px bg-slate-200"></span>
        <span class="bg-teal-500 text-white font-extrabold text-sm px-6 py-2.5 rounded-full">ثبت درخواست‌ های تجاری</span>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-5">

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-lg text-center">
          <template #header>
            <div class="flex justify-center pt-8">
              <svg class="w-24 h-24" viewBox="0 0 96 96">
                <path d="M16 30 20 14h56l4 16" fill="none" stroke="#f6a73c" stroke-width="2.5" stroke-linejoin="round" />
                <path d="M16 30a6 6 0 0 0 12 0 6 6 0 0 0 12 0 6 6 0 0 0 12 0 6 6 0 0 0 12 0 6 6 0 0 0 12 0" fill="none" stroke="#f6a73c" stroke-width="2.5" />
                <rect x="22" y="30" width="52" height="46" fill="#fff7ea" stroke="#f6a73c" stroke-width="2" />
                <rect x="40" y="52" width="16" height="24" fill="#fff" />
                <circle cx="68" cy="62" r="11" fill="#27b783" />
                <text x="68" y="67" font-size="13" font-weight="700" fill="#fff" text-anchor="middle">﷼</text>
              </svg>
            </div>
          </template>
          <template #title>
            <span class="text-[20px] font-extrabold text-amber-500">فرآیندهای صنفی</span>
            <div class="w-[60px] h-1 bg-amber-500 rounded mx-auto mt-2"></div>
          </template>
          <template #footer>
            <Button
              label="نمایش لیست درخواست‌ها"
              text
              class="!bg-slate-100 !border !border-slate-200 !rounded-xl !px-6 !py-3 !text-sm !font-bold !text-[#1c3a6b] hover:!bg-teal-50 hover:!border-teal-500 hover:!text-teal-600"
            >
              <template #icon>
                <svg class="w-4 h-4"><use href="#i-chevron" /></svg>
              </template>
            </Button>
          </template>
        </Card>

        
        <Card class="!rounded-2xl !border !border-slate-200 !shadow-lg text-center">
          <template #header>
            <div class="flex justify-center pt-8">
              <svg class="w-24 h-24" viewBox="0 0 96 96">
                <rect x="14" y="50" width="68" height="32" fill="#eef0fb" stroke="#5b4fd6" stroke-width="2" />
                <path d="M22 50V36l14 10V36l14 10V32l14 10V50" fill="none" stroke="#5b4fd6" stroke-width="2.5" stroke-linejoin="round" />
                <circle cx="64" cy="24" r="9" fill="none" stroke="#5b4fd6" stroke-width="2" />
                <path d="M55 24h18M64 15v18" stroke="#5b4fd6" stroke-width="1.5" />
                <line x1="14" y1="82" x2="82" y2="82" stroke="#5b4fd6" stroke-width="2.5" />
                <rect x="34" y="62" width="10" height="20" fill="#5b4fd6" />
              </svg>
            </div>
          </template>
          <template #title>
            <span class="text-[20px] font-extrabold text-[#1c3a6b]">بازرگانی و بهره‌برداری</span>
            <div class="w-[60px] h-1 bg-[#1c3a6b] rounded mx-auto mt-2"></div>
          </template>
          <template #footer>
            <Button
              label="نمایش لیست درخواست‌ها"
              text
              class="!bg-slate-100 !border !border-slate-200 !rounded-xl !px-6 !py-3 !text-sm !font-bold !text-[#1c3a6b] hover:!bg-teal-50 hover:!border-teal-500 hover:!text-teal-600"
            >
              <template #icon>
                <svg class="w-4 h-4"><use href="#i-chevron" /></svg>
              </template>
            </Button>
          </template>
        </Card>

      </div>
    </div>
  </section>
</template>
