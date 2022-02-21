<template>
  <div class="bg-gray-100 font-Lato">
    <TheNavbar/>
    <FadeTransition name="fade" mode="out-in">
    <Nuxt />
    </FadeTransition>
    <Footer/>
  </div>
</template>

<script>
import TheNavbar from "~/components/TheNavbar";
import FadeTransition from '~/transitions/FadeTransition'
import Footer from '~/components/Footer'

export default {
  components: {
    Footer,
    TheNavbar,
    FadeTransition
  },
}
</script>
<style>
.font-Lato{
  font-family: 'Lato';
}
</style>
