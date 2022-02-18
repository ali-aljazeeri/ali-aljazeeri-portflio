<template>
  <div class="bg-gray-100">
    <Container class="min-h-screen">
      <!--greeting-->
      <div class="flex flex-wrap flex-row justify-center items-center mt-5 w-full ">
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
    </Container>
  </div>
</template>

<script>

import Tutorial from '~/components/Tutorial'
import Container from '~/components/Container'

export default {
  name: 'IndexPage',
  components: {
    Container,
    Tutorial
  },
}
</script>

