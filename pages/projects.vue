<template>
  <div>
    <!--warper-->
    <div>Projects</div>
    <!--section title-->
    <div class="grid grid-cols-2 grid-flow-row space-y-5">
      <OrganismsProjectsCard
        card-title="Project 1"
        :technologies="['MongoDB', 'Express', 'React', 'Node']"
      />
      <OrganismsProjectsCard
        card-title="Project 2"
        :technologies="['MongoDB', 'Adonis', 'Nuxt', 'Node']"
      />
      <OrganismsProjectsCard card-title="Project 3" :technologies="['Vue', 'Node']" />
      <OrganismsProjectsCard
        card-title="Project 4"
        :technologies="['Mongo', 'Express', 'React', 'Node']"
      />
    </div>
  </div>
</template>
