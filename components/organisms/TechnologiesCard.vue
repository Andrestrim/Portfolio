<template>
  <div class="flex flex-col min-w-[194px] max-w-[256px] h-fit cardStyle">
    <h5 class="mb-4 text-[20px] text-white font-[PoppinsB] leading-tight">
      {{ sectionTitle }}
    </h5>
    <p class="mb-4 text-[#d2d4da]">Expertise with</p>
    <div class="flex flex-wrap gap-3 justify-evenly text-lg text-[#C8CAD1]">
      <p v-for="(tech, index) in technologies" :key="index">{{ tech }}</p>
    </div>
    <div v-if="isLearning">
      <p class="my-4 text-[#d2d4da]">Current learning</p>
      <div class="flex flex-wrap gap-3 justify-evenly text-lg text-[#C8CAD1]">
        <p v-for="(learn, index) in learning" :key="index">{{ learn }}</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import type { PropType } from "vue";
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    technologies: {
      default: ["Placeholder"],
      type: Array as PropType<String[]>,
    },
    sectionTitle: {
      default: "Card title",
      type: String,
    },
    learning: {
      default: ["num1", "num2"],
      type: Array as PropType<String[]>,
    },
    isLearning: {
      type: Boolean,
      default: false,
    },
  },
  setup(props) {
    const technologies = ref(props.technologies);
    const sectionTitle = ref(props.sectionTitle);
    const learning = ref(props.learning);
    const isLearning = ref(props.isLearning);
    return {
      technologies,
      sectionTitle,
      learning,
      isLearning,
    };
  },
});
</script>