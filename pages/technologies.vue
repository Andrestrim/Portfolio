<template>
  <!--warper-->
  <div>
    <!--section title-->
    <h5>Technologies</h5>
    <!--section Content-->
    <div class="flex justify-inline space-x-4">
        <OrganismsTechnologiesCard section-title="Front-end" :technologies="['Vue','typescript','Nuxt']"/>
        <OrganismsTechnologiesCard section-title="Back-end" :technologies="['Adonis','Node']"/>
        <OrganismsTechnologiesCard section-title="UI/UX" :technologies="['Figma']"/>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style scoped></style>
