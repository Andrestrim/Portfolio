<template>
  <div>
    <!--warper-->
    <div class="mb-3 titleGradient">Projects</div>
    <!--section title-->
    <div class="grid colunas">
      <OrganismsProjectsCard
        card-title="Project 1"
        :technologies="['MongoDB', 'Express', 'React', 'Node']"
      />
      <OrganismsProjectsCard
        card-title="Project 2"
        :technologies="['MongoDB', 'Adonis', 'Nuxt', 'Node']"
      />
      <OrganismsProjectsCard
        card-title="Project 3"
        :technologies="['Vue', 'Node']"
      />
      <OrganismsProjectsCard
        card-title="Project 4"
        :technologies="['Mongo', 'Express', 'React', 'Node']"
      />
    </div>
  </div>
</template>

<style scoped>
.colunas {
  grid-template-columns: repeat(auto-fit, minmax(10px,450px));
  grid-auto-rows: auto;
  gap: 20px;
}
</style>
