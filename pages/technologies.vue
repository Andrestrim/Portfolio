<template>
  <!--warper-->
  <div>
    <!--section title-->
    <h5 class="titleGradient">Technologies</h5>
    <!--section Content-->
    <div class="flex flex-wrap">
      <OrganismsTechnologiesCard
        class="grow my-5 mr-7"
        section-title="Front-end"
        :technologies="['javascript', 'typescript', 'Vue.js', 'Nuxt.js']"
        :is-learning="true"
        :learning="['React.js','Next.js']"
      />
      <OrganismsTechnologiesCard class="grow my-5 mr-7" section-title="Back-end"
      :technologies="['Node.js','Adonis.js','MySQL']"
      />

      <OrganismsTechnologiesCard
        class="grow my-5"
        section-title="UI/UX"
        :technologies="['Figma']"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style scoped></style>
