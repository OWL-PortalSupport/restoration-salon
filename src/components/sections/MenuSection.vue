<script setup lang="ts">
const osteopathyItems = [
  {
    name: '全身整体コース（標準）',
    time: '60 min',
    price: '¥7,700',
  },
  {
    name: '全身整体コース（集中）',
    time: '90 min',
    price: '¥11,000',
  },
  {
    name: '産後骨盤矯正',
    time: '50 min',
    price: '¥6,600',
  },
]

const relaxationItems = [
  {
    name: '深層筋もみほぐし',
    time: '60 min',
    price: '¥6,600',
  },
  {
    name: 'アロマオイルトリートメント',
    time: '90 min',
    price: '¥13,200',
  },
  {
    name: '足裏リフレクソロジー',
    time: '40 min',
    price: '¥4,400',
  },
]
</script>

<template>
  <section id="menu" class="bg-surface-container-low py-xl">
    <div class="mx-auto max-w-[1140px] px-gutter">
      <div class="mb-xl text-center">
        <h2 class="shinto-line mb-sm font-headline-lg text-headline-lg text-on-surface">
          メニュー
        </h2>

        <p class="mt-md text-on-surface-variant">
          心と身体を整え、本来の健やかさを取り戻すための多彩なメニュー
        </p>
      </div>

      <div class="mb-xl grid grid-cols-1 items-start gap-xl md:grid-cols-2">
        <div class="space-y-md">
          <span
            class="inline-block rounded-full bg-primary/10 px-4 py-1 font-label-md text-label-md text-primary"
          >
            Osteopathy
          </span>

          <h3 class="font-headline-md text-headline-md">整体・骨格調整</h3>

          <p class="text-body-md text-on-surface-variant">
            慢的な肩こりや腰痛、姿勢の乱れを根本から改善します。独自の解剖学的アプローチで、骨格と筋肉のバランスを緻密に調整し、疲れにくい身体へと導きます。
          </p>

          <img
            class="aspect-video w-full rounded-xl object-cover shadow-sm"
            alt="Professional hands performing an osteopathic adjustment."
            src="https://lh3.googleusercontent.com/aida-public/AB6AXuB6Cv23XtVxDG4uITQAdJXVml_86G8qymW2Sd-UmOPjGF8amIWoJr5rZT3A03LOeP7MD5e7qXZlnjy-D1fwLD01gASeyshmsmYmqxOhguXc8N0NGlPLrH9VOmhImV3zLTGaRdeJFeHrwuV_Y3ngZQPUcaFAEjpODer6acqDFKaUFH-LpyYrZgMYdSyxz6ffzrD8eo4PMJMEnVUTccXbmosGiCQr8En0VooUVHJjQxVCXzpqeXW-evGNymBWx8Zj7B5bzq4aVuUhInWn"
          />
        </div>

        <div class="rounded-xl border border-outline-variant/20 bg-surface p-md shadow-sm">
          <div class="divide-y divide-outline-variant/10">
            <div
              v-for="item in osteopathyItems"
              :key="item.name"
              class="flex items-center justify-between py-sm"
            >
              <div>
                <h4 class="font-bold">
                  {{ item.name }}
                </h4>

                <span class="text-xs text-on-surface-variant">
                  {{ item.time }}
                </span>
              </div>

              <div class="font-headline-md text-primary">
                {{ item.price }}
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="grid grid-cols-1 items-start gap-xl md:grid-cols-2">
        <div class="space-y-md md:order-2">
          <span
            class="inline-block rounded-full bg-secondary-container px-4 py-1 font-label-md text-label-md text-secondary"
          >
            Relaxation
          </span>

          <h3 class="font-headline-md text-headline-md">リラクゼーション</h3>

          <p class="text-body-md text-on-surface-variant">
            日々のストレスから解放される、至福のひととき。心地よいリズムの指圧とオイルトリートメントで、脳と身体を深いリラックス状態へと誘います。
          </p>

          <img
            class="aspect-video w-full rounded-xl object-cover shadow-sm"
            alt="Essential oils and professional spa setup."
            src="https://lh3.googleusercontent.com/aida-public/AB6AXuDOjFpdzLQ2OBMVjeSXs3SbpOPP6dvR-hJn0pBx3QP-s63ufqdmv7HJAvGmaV7loGhsiTZ2_l91LyKdA4ZC1Cg_bPPstYMyHcsEdA-vDP5oJ7ga0AA9difPcUIUMQjdeYDH6GFIBj4kBXyBVQL1-RKc73MzFrFYLO2Zv1IePQG9wI5bSZKEiXkWhYNHUPNhENLh9yKnTdP11J5uZXFi5VYYl8078pjqCnXNS3O9HYLVd1O8zLNkR_Tq2eVot2YtMDOO5Kct7-a5JfCO"
          />
        </div>

        <div
          class="rounded-xl border border-outline-variant/20 bg-surface p-md shadow-sm md:order-1"
        >
          <div class="divide-y divide-outline-variant/10">
            <div
              v-for="item in relaxationItems"
              :key="item.name"
              class="flex items-center justify-between py-sm"
            >
              <div>
                <h4 class="font-bold">
                  {{ item.name }}
                </h4>

                <span class="text-xs text-on-surface-variant">
                  {{ item.time }}
                </span>
              </div>

              <div class="font-headline-md text-secondary">
                {{ item.price }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
