<template>
  <div class="bg-gray-100">
    <Container class="min-h-screen">
      <!--greeting-->
      <div class="flex flex-wrap flex-row justify-center items-center mt-5 w-full">
        <!--image-->
        <div class="md:w-1/2 w-full flex justify-center items-center">
          <img src="../static/memoji.png" class="md:w-96 w-52"/>
        </div>
        <!--hello-->
        <div class="md:w-1/2 w-full flex flex-col justify-center mt-3">
          <p class="text-gray-900 w-full md:text-left text-center text-2xl font-bold">HELLO THERE 👋 I'm </p>
          <p class="text-gray-900 w-full md:text-left text-center text-5xl font-bold mt-3">Ali Aljazeeri</p>
          <p class="text-green-500 w-full md:text-left text-center text-2xl font-bold mt-3">Developer 👨‍💻</p>
          <p class="text-green-500 w-full md:text-left text-center text-lg font-bold mt-3">Tech lover , Seeking
            challenges and knowledge</p>
        </div>
      </div>
      <!--projects-->
      <h1 class="flex items-center font-bold mt-20">
        <!--general icon-->
        <span>
          <svg xmlns="http://www.w3.org/2000/svg" width="24" fill="#111827" viewBox="0 0 384 512"><!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path
            d="M384 48V512l-192-112L0 512V48C0 21.5 21.5 0 48 0h288C362.5 0 384 21.5 384 48z"
          /></svg>
        </span>
        <!--general tittle-->
        <span class="ml-2 text-lg text-gray-900">Projects</span>
      </h1>
      <!--projects list-->
      <div class="flex flex-row flex-wrap">
        <Project class="xl:w-1/3 md:w-1/2 w-full" v-for="p in projects" :project="p" :key="p.title"></Project>
      </div>
    </Container>
  </div>
</template>

<script>

import Container from '~/components/Container'
import Project from '~/components/Project'
import json from '~/json/projects.json'

export default {
  name: 'IndexPage',
  components: {
    Container,
    Project
  },
  data () {
    return {
      projects : json
    }
  }
}
</script>

