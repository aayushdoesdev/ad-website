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
    class="max-w-7xl mx-auto py-10 flex flex-col items-center justify-center text-center font-Grotesque font-semibold text-white px-4 xl:px-0"
  >
    <h1 class="title-text mb-4">
      Why Aren't You Landing High-<br />Ticket Projects?
    </h1>
    <div class="w-full">
      <div
        v-for="value in list"
        :key="value"
        class="flex items-center justify-center"
      >
        <div class="bg-white w-full flex gap-3 mt-6">
          <span class="bg-[#E4F00A] p-4"
            ><img src="/svg/question.svg" alt="" class="max-w-[20px]"
          /></span>
          <p class="md:text-[20px] xl:text-[29px] p-4 text-left text-black">{{ value }}</p>
        </div>
      </div>
    </div>
    <h1 class="title-text mt-4">
      Even the best skills won't land you premium clients —<br />
      your proposal is your pitch.
    </h1>
  </section>
</template>
