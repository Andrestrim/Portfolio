<template>
  <div
    class="flex flex-col min-w-[194px] max-w-[256px] h-auto cardStyle"
  >
    <h5
      class="mb-4 text-[20px] text-white font-[PoppinsB] leading-tight"
    >
      {{ sectionTitle }}
    </h5>
    <div class="flex flex-wrap gap-3 justify-evenly text-lg text-[#C8CAD1]">
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

<style scoped>
.namedCard {
  grid-template-columns: repeat(auto-fit, minmax(4px,85px));
  grid-auto-rows: auto;
  gap: 10px;
}
</style>
