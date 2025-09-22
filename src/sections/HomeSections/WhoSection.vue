<script setup>
const whyList = [
  {
    title: "Freelancers tired of low-paying gigs",
    img: "/svg/who1.svg",
  },
  {
    title: "Agencies who want faster conversions",
    img: "/svg/who2.svg",
  },
  {
    title: "Creatives who struggle to explain their value",
    img: "/svg/who3.svg",
  },
  {
    title: "Anyone unsure what to say in a proposal",
    img: "/svg/who4.svg",
  },
];
</script>

<template>
  <section
    class="max-w-7xl mx-auto py-20 flex flex-col items-center justify-center text-center font-Grotesque font-semibold text-white"
  >
    <div class="">
      <h1 class="text-[60px]">Who It’s For</h1>

      <div class="grid grid-cols-2 gap-x-12 gap-y-10 mt-16 w-full">
        <div
          v-for="item in whyList"
          :key="item.title"
          class="flex items-center gap-4"
        >
          <img :src="item.img" alt="" class="w-16 h-16 object-cover" />
          <p class="text-[30px] text-left">{{ item.title }}</p>
        </div>
      </div>
    </div>

    <div class="mt-24 w-full">
        <h1 class="text-[60px]">Real Results</h1>

        <div class="grid grid-cols-3 gap-6 mt-10">
            <div class="space-y-3">
                <div class="w-full h-[100px] bg-slate-400"></div>
                <p class="text-[20px]">I sent one proposal from this playbook and landed a $3,000 project the next day</p>
                <p class="text-[#E4F00A]">– Abhisek Soni, Digital Marketer</p>
            </div>
            <div class="space-y-3">
                <div class="w-full h-[100px] bg-slate-400"></div>
                <p class="text-[20px]">I sent one proposal from this playbook and landed a $3,000 project the next day</p>
                <p class="text-[#E4F00A]">– Abhisek Soni, Digital Marketer</p>
            </div>
            <div class="space-y-3">
                <div class="w-full h-[100px] bg-slate-400"></div>
                <p class="text-[20px]">I sent one proposal from this playbook and landed a $3,000 project the next day</p>
                <p class="text-[#E4F00A]">– Abhisek Soni, Digital Marketer</p>
            </div>
        </div>
    </div>
  </section>
</template>
