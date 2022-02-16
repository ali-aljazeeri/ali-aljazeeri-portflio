<template>
  <div class="bg-gray-100 font-Lato">
    <TheNavbar/>
    <Nuxt />
  </div>
</template>

<script>
import TheNavbar from "~/components/TheNavbar";

export default {
  components: {
    TheNavbar
  },
}
</script>
<style>
.font-Lato{
  font-family: 'Lato';
}
</style>
