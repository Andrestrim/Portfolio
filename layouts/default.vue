<template>
  <div class="max-w-full flex flex-col">
    <OrganismsHeader class="items-start mx-4 mt-3" />
    <div class="block">
      <slot />
    </div>
    <OrganismsFooter class="items-end" />
  </div>
</template>

<script>
import "@/assets/css/main.css";
</script>
