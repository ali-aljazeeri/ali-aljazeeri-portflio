<template>
  <container class="my-16 flex flex-row flex-wrap justify-center text-gray-900 text-center md:text-xl text-lg">
    <p class="font-semibold w-full" v-if="currentRoute !== 'project'">Say hello 👋</p>
    <p class="font-semibold w-full" v-if="currentRoute === 'project'">Feedback? 🤔</p>
    <a href="mailto:alijaz1999@gmail.com" class="w-full">alijaz1999@gmail.com</a>
  </container>
</template>

<script>
import Container from '~/components/Container'

export default {
  name: 'Footer',
  components: { Container },
  computed: {
    currentRoute () {
      let p = this.$route.fullPath.split('/')
      return p[1]
    }
  },

}
</script>

<style scoped>

</style>
