<script setup lang="ts">
const flowItems = [
  {
    number: '1',
    title: 'ご来店・受付',
    text: '笑顔でスタッフがお迎えします。まずは心地よい空間で一息ついてください。',
    alt: 'A warm, friendly Japanese receptionist smiling behind a minimalist wooden counter.',
    image:
      'https://lh3.googleusercontent.com/aida-public/AB6AXuCue_nGG4SccmmCQ3EJbF_nhoBaVIXSpOZKjXtaMOoSk8IvtgPRCllImv8Fkr2jRI_QnvpYFuFZ0jjeFmWKrRUwMNmmVxiP043EaE1GRmchu7JrS9eS7PIL15_FtLlE4g8dz7eDyWjnmc97uEpHWzxyHfygqwwhvNr3vdEo_ojbgOB3oz68Xr8FwA4r03ii3a6kUjcXtB1lce1M2HhmWtCwjaaBj05FoG2gMtfabZZzMJruJjdBJAfYZSZMBwtGEIeP2BuoGEySXk-7',
  },
  {
    number: '2',
    title: 'カウンセリング',
    text: '現在のお悩みや生活習慣を丁寧にお伺いし、最適なプランをご提案します。',
    alt: 'A professional therapist in a clean uniform sitting across from a client for counseling.',
    image:
      'https://lh3.googleusercontent.com/aida-public/AB6AXuCgMvYrolVSwRk1xmJyvztekZyw7q4NzINVJg_pQDTb8f5OV0-_OgitfRbjfNdZmBQ246UAcZ0HJ2DJVXjRkpK5ucJMonE9gERLoKyT3lFM1CckBJE012zt0JG9jHvbbZjU0RJ1DdgRsfSfLUhN2mdmoTu7QQdLrNdWYN9qrz1w4SI0-blx4saaFQAI87uQH37WQesZeVQxj1n-lK6TE6hOILpxyUF2m8IkBe_vO4oUVlICLNiW1LtMTVGAJAUw2juCNfqs_IdCOoLW',
  },
  {
    number: '3',
    title: '施術',
    text: 'お一人おひとりの状態に合わせ、根本から整える専門的な手技を行います。',
    alt: 'A close-up shot of a therapeutic treatment in progress.',
    image:
      'https://lh3.googleusercontent.com/aida-public/AB6AXuAautTmjMKuevU0TsR3ooMqmyEUT28gRcndqWehc4P5r8Y0fqnHDFSP7gxxjbrbvgGpzTWW74Bzgnb-KhIf5Pj5Nd5lGjylV_VXkhRvNAMy3ifM1pHhRbyRbSwEwWL4gpAwBmC3jLRba8aSyJIPxJZM-wO4Ef5FWz07qVi88o1P0riVeggTRbcEnEyX0bSW1C_J0L8iw654vYDd6WGk5gH_IYAa1hxmLLCbspsuTkHnkGeeQ_DpnzlS3FszY1A7A2uJ0NrRa1Dn1fY9',
  },
  {
    number: '4',
    title: 'アフターケア',
    text: '良い状態を維持するためのアドバイスをお伝えし、お茶でリラックス。',
    alt: 'A client enjoying a cup of herbal tea after a treatment.',
    image:
      'https://lh3.googleusercontent.com/aida-public/AB6AXuDcJYpozq4dpwD2lhaX2AhSDMFXSR461BN4WSgXLkf1QxwGz3DDhwpibtzEZ0llPpw-33q-_h7sB7Jal05BmSQ2Z8okwDA5IbPNG3ILGHUHBK3lsqTGxiAVBHD3GUWYWWDqYGGpoWYNvVlacKBhpGcbBmkHR7wB71fTZqurY0l0AcFzWM8BPo4ZrJCN9eADPIyvb37xa3eoQEDDkgKvs3mEWKMh7Lo-le8urnsLDWpFQQgKKbwH1TbKlomMKy7aeEN2IVjTIRZbN4BN',
  },
]
</script>

<template>
  <section id="flow" class="bg-surface py-xl">
    <div class="mx-auto max-w-[1140px] px-gutter">
      <div class="mb-xl text-center">
        <p class="mb-sm font-label-md text-label-md uppercase tracking-[0.2em] text-primary">
          Flow
        </p>

        <h2 class="shinto-line font-headline-lg text-headline-lg text-on-surface">施術の流れ</h2>

        <p class="mt-md text-on-surface-variant">
          初めての方でも、安心してゆったりとお過ごしいただけます。
        </p>
      </div>

      <div class="relative grid grid-cols-1 gap-margin md:grid-cols-4">
        <div
          v-for="item in flowItems"
          :key="item.number"
          class="flex flex-col items-center text-center"
        >
          <div
            class="mb-md aspect-[3/4] w-full overflow-hidden rounded-xl border border-outline-variant"
          >
            <img
              :src="item.image"
              :alt="item.alt"
              class="h-full w-full object-cover transition-transform duration-500 hover:scale-105"
            />
          </div>

          <div class="mb-sm">
            <span
              class="inline-flex h-8 w-8 items-center justify-center rounded-full bg-primary text-sm font-bold text-white"
            >
              {{ item.number }}
            </span>
          </div>

          <h3 class="mb-xs font-headline-md text-headline-md">
            {{ item.title }}
          </h3>

          <p class="text-sm text-on-surface-variant">
            {{ item.text }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
