<script setup>
const list = [
  "Are you sending the same generic proposals as everyone else?",
  "Do your pitches fail to stand out or show real value?",
  "Are you struggling to explain why you're worth the premium rate?",
  "Are clients ghosting you after the first message?",
  "Are you unsure what to write or how to structure your proposal?",
];
</script>

<template>
  <section
    class="max-w-7xl mx-auto py-20 flex flex-col items-center justify-center text-center font-Grotesque font-semibold text-white"
  >
    <h1 class="text-[60px]">
      Why Aren't You Landing High-<br />Ticket Projects?
    </h1>

    <div class="mt-16 w-full">
      <div
        v-for="value in list"
        class="flex items-center justify-center space-y-6"
      >
        <div class="bg-[#E4F00A] p-4 mt-6">
          <img src="/svg/question.svg" alt="" />
        </div>
        <div class="bg-white p-4 w-full">
          <p class="text-[29px] text-left text-black">{{ value }}</p>
        </div>
      </div>
    </div>

    <h1 class="text-[60px] mt-16">
      Even the best skills won't land you premium clients —<br/> your proposal is
      your pitch.
    </h1>
  </section>
</template>
