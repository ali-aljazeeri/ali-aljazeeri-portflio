<template>
  <div class="bg-gray-100 font-Lato">
    <TheNavbar/>
    <Tutorial/>
  </div>
</template>

<script>
import TheNavbar from "~/components/TheNavbar";
import Tutorial from "~/components/Tutorial";

export default {
  name: 'IndexPage',
  components: {
    TheNavbar,
    Tutorial
  },
}
</script>
<style>
.font-Lato{
  font-family: 'Lato';
}
</style>
