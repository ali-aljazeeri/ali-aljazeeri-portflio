<template>
  <Container class="">
    <div class="h-16 flex items-center justify-between px-2">
      <!--return button to home page-->
      <div v-if="currentRoute !== '/'">
        <nuxt-link to="/">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
            <path d="M0 0h24v24H0z" fill="none"></path>
            <path d="M21 11H6.83l3.58-3.59L9 6l-6 6 6 6 1.41-1.41L6.83 13H21z"></path>
          </svg>
        </nuxt-link>
      </div>

      <!--return button to home page-->

      <div v-if="currentRoute === '/'">
        <nuxt-link to="/">
          <p class="font-semibold text-gray-900 md:text-lg text-base"><span class="text-green-500">Al</span>jazeer<span
            class="text-green-500"
          >i</span></p>
        </nuxt-link>
      </div>

      <!--about page -->
      <div v-if="currentRoute === '/'">
        <nuxt-link to="about">
          <p class="font-semibold text-gray-400 md:text-lg text-base">About</p>
        </nuxt-link>
      </div>


    </div>

    <div class="h-0.5 bg-gray-900" v-if="currentRoute === '/'"></div>

  </Container>
</template>

<script>


import Container from '~/components/Container'

export default {
  name: 'TheNavbar',
  components: {
    Container,
  },
  computed: {
    currentRoute () {
      return this.$route.fullPath
    }
  },

}
</script>

<style scoped>

</style>
