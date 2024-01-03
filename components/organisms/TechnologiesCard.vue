<template>
  <div
    class="block w-64 h-auto rounded-lg bg-white p-6 shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700"
  >
    <h5
      class="mb-2 text-xl font-medium leading-tight text-neutral-800 dark:text-neutral-50"
    >
      {{ sectionTitle }}
    </h5>
    <div class="grid grid-flow-col justify-center my-3 space-x-2">
      <p v-for="(tech, index) in technologies" :key="index">{{ tech }}</p>
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
  },
  setup(props) {
    const technologies = ref(props.technologies);
    const sectionTitle = ref(props.sectionTitle);
    return {
      technologies,
      sectionTitle,
    };
  },
});
</script>

<style scoped></style>
