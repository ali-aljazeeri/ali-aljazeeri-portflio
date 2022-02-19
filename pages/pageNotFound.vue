<template>
  <container class="min-h-screen flex justify-center items-center -mt-16">
    <div class="text-gray-900 text-center text-lg font-semibold w-full">ERROR 404 :page not found <br/>
      <nuxt-link to="/">
        <h1 class="text-gray-900 text-center text-base underline mt-2 w-full">Back to home page</h1>
      </nuxt-link>
    </div>
  </container>
</template>

<script>
import Container from '~/components/Container'

export default {
  name: 'pageNotFound',
  components: { Container }
}
</script>

<style scoped>

</style>
