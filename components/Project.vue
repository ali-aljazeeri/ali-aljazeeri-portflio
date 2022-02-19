<template>
  <div class="mt-10 lg:px-16 flex flex-col justify-between md:px-10">
    <!--image-->
    <div class="rounded-xl h-44 w-full">
      <img :alt="project.title" :src="require(`~/assets/${project.coverImage}`)"
           class="object-cover w-full h-44 rounded-xl border border-gray-900"
      >
    </div>
    <!--general info-->
    <div class="flex flex-col justify-between flex-1 mt-3">
      <div>
        <!--title-->
        <p class="text-gray-900 font-bold md:text-xl text-lg text-left w-full">{{ project.title }}</p>
        <!--title-->
        <p class="text-gray-900 font-semibold md:text-lg text-base text-left w-full">Developed using :
          <span class="font-normal">{{ project.developedUsing }}</span>
        </p>
      </div>
      <!--more info redirect to project/name-->
      <nuxt-link :to="'/project/'+project.name">
        <div class="mt-3 bg-gray-900 rounded-xl hover:bg-black p-3">
          <p class="text-white font-semibold md:text-xl text-lg text-center w-full">More Information</p>
        </div>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Project',
  props: ['project'],
}
</script>

<style scoped>

</style>
