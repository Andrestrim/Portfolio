<template>
  <div
    class="flex flex-col min-w-[24rem] max-w-fit h-auto cardStyle"
  >
      <img
        class="rounded-t-lg max-w-[400px] h-52"
        src="https://tecdn.b-cdn.net/img/new/standard/nature/184.jpg"
        alt=""
      />
    <div class="p-6">
      <h5
        class="mb-2 text-xl font-medium leading-tight text-neutral-800 dark:text-neutral-50"
      >
        {{ cardTitle }}
      </h5>
      <p class="mb-4 text-base text-neutral-600 dark:text-neutral-200">
        {{ cardDescription }}
      </p>
      <div class="my-4 flex justify-center">
        <div class="inline-flex space-x-10">
          <div v-for="(tech,index) in techData" :key="index">{{ tech }}</div>
        </div>
      </div>

      <div class="mt-10 w-full flex justify-between">
        <AtomsButton btText="See Project"/>
        <AtomsButton btText="Source Code"/>
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
      default: ["placeholder"],
      type: Array as PropType<String[]>,
    },
    cardTitle: {
      default: "Card title",
      type: String,
    },
    cardDescription:{
      default: "Us simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and it to make a type specimen book. It has survived not only five centuries, but also the leap into.",
      type: String,
    },
  },
  setup(props){
    const techData = ref(props.technologies);
    const cardTitle = ref(props.cardTitle);
    const cardDescription = ref(props.cardDescription)
    return{
      techData,
      cardTitle,
      cardDescription
    }
  }
});
</script>

<!--rounded-lg bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700  ////card class-->