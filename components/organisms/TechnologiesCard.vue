<template>
  <div
    class="block w-64 h-auto rounded-lg py-6 pl-6 pr-1 border-1 border-[#1D212C] bg-[#596074] shadow-[12px_17px_17px_-7px_#252525]"
  >
    <h5
      class="mb-4 text-[20px] text-[#C9AD8B] font-[PoppinsB] leading-tight"
    >
      {{ sectionTitle }}
    </h5>
    <div class="grid text-lg font-[Poppins] text-white  namedCard">
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
