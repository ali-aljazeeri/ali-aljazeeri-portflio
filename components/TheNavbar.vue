<template>
  <Container class="">
    <div class="h-16 flex items-center justify-between">
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
        <p class="font-semibold text-gray-900 md:text-lg text-base">Ali Aljazeeri</p>
      </div>

      <!--return button to home page-->
      <div v-if="currentRoute === '/'">
        <p class="font-semibold text-gray-400 md:text-lg text-base">About</p>
      </div>


    </div>
    <div class="h-0.5 bg-gray-900"></div>

  </Container>
</template>

<script>


import Container from "~/components/Container";

export default {
  name: "TheNavbar",
  components: {
    Container
  },
  computed: {
    currentRoute() {
      return this.$route.fullPath
    }
  },

}
</script>

<style scoped>

</style>
