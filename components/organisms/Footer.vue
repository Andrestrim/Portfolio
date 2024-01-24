<template>
<footer
  class="flex flex-col items-center text-center text-white">
  <div class="container pt-16">
    <div class="mb-2 flex justify-center">
      <MoleculesSocialLinks />
    </div>
  </div>

  <!--Copyright section-->
  <div
    class="w-full p-4 text-center text-white">
    @{{ year }} André Figueiredo, All rights reserved.
  </div>
</footer>
</template>

<script lang="ts">
const currentDate = new Date()
const year = currentDate.getFullYear()

export default{
  setup(){
    return{
      year,
    }
  }
}
</script>v3