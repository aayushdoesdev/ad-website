<script setup>
import { ref } from "vue";

const faqList = [
  {
    question: "What exactly is the Proposal Playbook?",
    answer:
      "The Proposal Playbook is a comprehensive guide with templates and strategies for winning client proposals.",
  },
  {
    question: "Who is this playbook for?",
    answer:
      "It's designed for freelancers, agencies, and anyone looking to improve their proposal process.",
  },
  {
    question: "Is it beginner-friendly?",
    answer:
      "Absolutely. It includes step-by-step instructions perfect for beginners.",
  },
  {
    question: "How will I receive the playbook?",
    answer:
      "After purchase, you'll receive an instant digital download via email.",
  },
  {
    question: "Can I customize the templates?",
    answer: "Yes, all templates are fully editable to suit your needs.",
  },
  {
    question: "Will this guarantee I get clients?",
    answer:
      "While the playbook increases your chances, there are no guarantees in sales.",
  },
  {
    question: "Do you offer refunds?",
    answer: "Due to the digital nature, refunds are not offered.",
  },
];

const openIdx = ref(null);

function toggle(idx) {
  if (openIdx.value === idx) {
    openIdx.value = null;
  } else {
    openIdx.value = idx;
  }
}
</script>

<template>
  <section class="bg-white font-Grotesque text-center font-semibold">
    <div class="max-w-7xl mx-auto py-20">
      <h1 class="text-[60px]">Frequently asked questions</h1>
      <div class="mt-24 space-y-6">
        <div v-for="(item, idx) in faqList" :key="idx" class="flex items-start">
          <div
            class="w-full bg-black text-white p-4 cursor-pointer"
            @click="toggle(idx)"
          >
            <p class="text-[25px] text-left">{{ item.question }}</p>
            <transition name="fade">
              <div
                v-if="openIdx === idx"
                class="text-[20px] text-left mt-4 text-gray-200 font-normal"
              >
                {{ item.answer }}
              </div>
            </transition>
          </div>
          <div
            class="px-4 py-5 bg-[#E4F00A] cursor-pointer"
            @click="toggle(idx)"
          >
            <img
              :class="
                openIdx === idx
                  ? 'rotate-45 transition-transform'
                  : 'transition-transform'
              "
              src="/svg/plus.svg"
              alt=""
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
