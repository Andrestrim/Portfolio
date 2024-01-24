<template>
  <div class="grid relative grid-cols-2">
    <div class="flex flex-col relative w-full">
      <div class="">
        <p class="text-[28px] font-[PoppinsB]">Welcome to my portfolio !</p>
      </div>

      <div class="my-6 space-y-4">
        <p>
          Hey there! My name is André Figueiredo, I have a BS in information
          systems.
        </p>
        <p>
          I started studying and creating my own projects since March 2022, and
          since then, I feel more and more inspired and willing to pursue my
          career in the area as a full-stack developer.
        </p>
        <p>My current goal is to kickstart my career and get my first job.</p>
        <p>
          My main technologies are Javascript/Typescript, Vue, Nuxt.js,
          Adonis.js and Node.js.
        </p>
      </div>

      <div class="space-x-3 flex cursor-pointer relative">
        <AtomsButton btText="More About me" link="/about" />
        <AtomsButton btText="My Projects" link="/projects" />
      </div>
    </div>

    <img src="@/assets/images/Bg-icon.svg" alt="" />
  </div>
</template>
