<template>
  <Container class="min-h-screen lg:w-3/5 md:w-4/6" v-if="project">
    <!--logo-->
    <div class="md:h-28 h-20 flex md:justify-start justify-center items-center ">
      <img :alt="project.title" :src="require(`~/assets/${project.logo}`)" class="h-full">
    </div>
    <!--info-->
    <div class="flex flex-row flex-wrap items-center justify-between md:text-lg text-base text-gray-900">
      <!--project name-->
      <div class="md:w-1/2 w-full flex flex-row flex-wrap md:text-left text-center mt-3">
        <p class="font-semibold  w-full">Project Name:</p>
        <p class=" w-full">{{project.title}}</p>
      </div>
      <!--project year-->
      <div class="md:w-1/2 w-full flex flex-row flex-wrap md:text-right text-center mt-3">
        <p class="font-semibold  w-full">Year</p>
        <p class=" w-full">{{ project.year }}</p>
      </div>
    </div>
    <!--line-->
    <div class="h-0.5 bg-gray-900 mt-2 "></div>
    <!--description-->
    <div class="md:text-lg text-base text-gray-900 flex flex-row flex-wrap text-left mt-3" v-for="d in project.description">
      <p class="font-semibold w-full"><span v-html="d.title"></span></p>
      <p class="w-full mt-1"><span v-html="d.text"></span></p>
    </div>
    <!--images-->
    <div class="md:text-lg text-base text-gray-900 flex flex-row flex-wrap text-left mt-5" v-if="project.images">
      <p class="font-semibold w-full" v-if="project.images.length === 1">Project Image</p>
      <p class="font-semibold w-full" v-if="project.images.length > 1">Project Images</p>
    </div>
    <!--line-->
    <div class="h-0.5 bg-gray-900 mt-2 " v-if="project.images"></div>

    <div class="md:text-lg text-base text-gray-900 flex flex-row flex-wrap text-left mt-3 w-full"v-for="i in project.images" >
      <p class="font-semibold w-full" v-if="i.title"><span v-html="i.title"></span></p>
      <p class="w-full mt-1" v-if="i.text"><span v-html="i.text"></span></p>
      <div class="mt-1 flex justify-center items-center bg-gray-900 lg:py-10 md:py-5 p-3 rounded-xl w-full">
        <img :alt="project.title" :src="require(`~/assets/${i.image}`)" class="md:w-4/5 ">
      </div>
    </div>

  </Container>
</template>

<script>
import Container from '~/components/Container'
import json from '~/json/projects.json'
export default {
  name: 'index',
  components: { Container },
  data () {
    return {
      projects: json,
      project : undefined,
    }
  },
  computed: {
    name () {
      return this.$route.params.name
    }
  },
  created () {
    this.getProject()
  },
  methods:{
    getProject(){
      let n= this.name
      this.project = this.projects[n]
      if (this.project === undefined)
      {
        this.$router.push('/')
      }
    }
  }

}
</script>

<style scoped>

</style>
