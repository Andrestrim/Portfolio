<template>
  <div class="flex flex-col h-screen">
    <OrganismsHeader class="items-start mx-4 mt-3" />
    <div class="block mx-32 mt-20 flex-grow">
      <slot />
    </div>
    <OrganismsFooter class="" />
  </div>
</template>

<script>
import "@/assets/css/main.css";
</script>
