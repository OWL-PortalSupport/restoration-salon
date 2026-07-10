<template>
  <footer id="footer" class="w-full bg-surface-container-highest py-lg">
    <div
      class="mx-auto mb-md flex max-w-[1140px] flex-col justify-between gap-md border-b border-outline-variant px-gutter pb-md md:flex-row"
    >
      <div class="w-full md:w-[420px] md:flex-none">
        <div class="mb-sm font-headline-sm text-headline-sm font-semibold text-on-surface">
          Restoration Salon
        </div>

        <p
          class="mb-md w-full text-sm leading-7 whitespace-normal break-normal text-on-surface-variant"
        >
          心と身体を整える、現代の隠れ家。<br />
          あなたの「休息」を専門的にサポートします。
        </p>
      </div>

      <div class="grid grid-cols-1 gap-lg md:grid-cols-1">
        <div class="flex flex-col gap-sm">
          <a
            class="text-sm text-on-surface-variant transition-colors hover:text-primary"
            href="#hero"
          >
            Top
          </a>

          <a
            class="text-sm text-on-surface-variant transition-colors hover:text-primary"
            href="#flow"
          >
            Flow
          </a>

          <a
            class="text-sm text-on-surface-variant transition-colors hover:text-primary"
            href="#menu"
          >
            Menu
          </a>

          <a
            class="text-sm text-on-surface-variant transition-colors hover:text-primary"
            href="#access"
          >
            Access
          </a>
        </div>
      </div>
    </div>

    <div class="mx-auto max-w-[1140px] px-gutter text-center md:text-left">
      <p class="text-xs text-on-surface-variant opacity-60">
        © 2026 Restoration Salon. All rights reserved.
      </p>
    </div>
  </footer>

  <div
    class="fixed bottom-0 left-0 z-50 flex w-full items-center justify-between bg-primary p-sm text-on-primary md:hidden"
  >
    <div class="text-xs">
      <p class="font-bold leading-tight">心身の調和をあなたに</p>
      <p class="opacity-80">初回限定キャンペーン中</p>
    </div>

    <button
      type="button"
      class="rounded-full bg-secondary-container px-md py-xs text-sm font-bold text-on-secondary-container"
    >
      今すぐ予約
    </button>
  </div>
</template>
