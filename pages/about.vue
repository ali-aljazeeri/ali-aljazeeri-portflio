<template>
  <div>
    <container>
      <!--about me-->
      <div class="text-lg font-bold text-gray-900 text-center mt-5">
        My name is Ali Isa Aljazeeri 👋<br/>
        A computer science student , always looking for a challenge and something new to learn 🤓<br/>
        I will always try to volunteer and make a difference 🌎<br/>
        Video games lover and Final Fantasy 14 addict 🎮<br/>
        Formula 1 fan 🏎️<br/>
      </div>
    </container>
    <Container class="min-h-screen flex flex-row flex-wrap text-gray-900">
      <!--work-->
      <div class="flex flex-col w-full md:w-1/2 mt-10">
        <h1 class="flex items-center font-bold">
          <!--general icon-->
          <span>
          <svg xmlns="http://www.w3.org/2000/svg" width="24" fill="#111827" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path
            d="M320 336c0 8.844-7.156 16-16 16h-96C199.2 352 192 344.8 192 336V288H0v144C0 457.6 22.41 480 48 480h416c25.59 0 48-22.41 48-48V288h-192V336zM464 96H384V48C384 22.41 361.6 0 336 0h-160C150.4 0 128 22.41 128 48V96H48C22.41 96 0 118.4 0 144V256h512V144C512 118.4 489.6 96 464 96zM336 96h-160V48h160V96z"
          /></svg>
        </span>
          <!--general tittle-->
          <span class="ml-2">Work</span>
        </h1>

        <div class="flex mt-6 flex-1">
          <!--the gray line-->
          <div class="relative bg-gray-500 opacity-25 rounded-full w-1 left-2"></div>

          <div class="flex flex-col">

            <!--object-->
            <div class="flex py-4" v-for="info in about.work">
              <!--dot-->
              <div class="z-10 flex-shrink-0 mt-5 w-3 h-3 bg-gray-900 rounded-full"></div>
              <div class="ml-8">

                <!--logo-->
                <a :href="'https://'+info.link" target="_blank">
                  <img :alt="info.organization" :src="require(`~/assets/${info.logo}`)" class="h-16 w-auto p-2">
                </a>
                <div class="mt-2">
                  <!--title-->
                  <h2 class="font-bold">{{ info.title }}</h2>
                  <!--date-->
                  <span class="text-sm font-light whitespace-no-wrap">{{ info.date }}</span>
                </div>

                <div class="text-sm">
                  <!--organization-->
                  <div class="mt-2">{{ info.organization }}</div>
                  <!--work done-->
                  <ul class="mt-2 text-xs list-disc list-inside" v-for="x in info.work">
                    <li><span v-html="x"></span></li>
                  </ul>
                </div>
              </div>
              <!--end object-->
            </div>
          </div>
        </div>
        <!--end work-->
      </div>


      <!--education-->
      <div class="flex flex-col w-full md:w-1/2 mt-10">
        <h1 class="flex items-center font-bold">
          <!--general icon-->
          <span>
          <svg xmlns="http://www.w3.org/2000/svg" width="24" fill="#111827" viewBox="0 0 640 512"><!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path
            d="M623.1 136.9l-282.7-101.2c-13.73-4.91-28.7-4.91-42.43 0L16.05 136.9C6.438 140.4 0 149.6 0 160s6.438 19.65 16.05 23.09L76.07 204.6c-11.89 15.8-20.26 34.16-24.55 53.95C40.05 263.4 32 274.8 32 288c0 9.953 4.814 18.49 11.94 24.36l-24.83 149C17.48 471.1 25 480 34.89 480H93.11c9.887 0 17.41-8.879 15.78-18.63l-24.83-149C91.19 306.5 96 297.1 96 288c0-10.29-5.174-19.03-12.72-24.89c4.252-17.76 12.88-33.82 24.94-47.03l190.6 68.23c13.73 4.91 28.7 4.91 42.43 0l282.7-101.2C633.6 179.6 640 170.4 640 160S633.6 140.4 623.1 136.9zM351.1 314.4C341.7 318.1 330.9 320 320 320c-10.92 0-21.69-1.867-32-5.555L142.8 262.5L128 405.3C128 446.6 213.1 480 320 480c105.1 0 192-33.4 192-74.67l-14.78-142.9L351.1 314.4z"
          />
          </svg>
        </span>
          <!--general tittle-->
          <span class="ml-2">Education</span>
        </h1>

        <div class="flex mt-6 flex-1">
          <!--the gray line-->
          <div class="relative bg-gray-500 opacity-25 rounded-full w-1 left-2"></div>

          <div class="flex flex-col">

            <!--object-->
            <div class="flex py-4" v-for="info in about.education">
              <!--dot-->
              <div class="z-10 flex-shrink-0 mt-5 w-3 h-3 bg-gray-900 rounded-full"></div>
              <div class="ml-8">

                <!--logo-->
                <a :href="'https://'+info.link" target="_blank">
                  <img :alt="info.organization" :src="require(`~/assets/${info.logo}`)" class="h-16 w-auto p-2">
                </a>
                <div class="mt-2">
                  <!--title-->
                  <h2 class="font-bold">{{ info.title }}</h2>
                  <!--date-->
                  <span class="text-sm font-light whitespace-no-wrap">{{ info.date }}</span>
                </div>

                <div class="text-sm">
                  <!--organization-->
                  <div class="mt-2">{{ info.organization }}</div>
                  <!--work done-->
                  <ul class="mt-2 text-xs list-disc list-inside" v-for="x in info.work">
                    <li>{{ x }}</li>
                  </ul>
                </div>
              </div>
              <!--end object-->
            </div>
          </div>
        </div>
        <!--end education-->
      </div>

      <!--volunteer-->
      <div class="flex flex-col w-full md:w-1/2 my-10">
        <h1 class="flex items-center font-bold">
          <!--general icon-->
          <span>
          <svg xmlns="http://www.w3.org/2000/svg" width="24" fill="#111827" viewBox="0 0 640 512"><!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path
            d="M488 191.1h-152l.0001 51.86c.0001 37.66-27.08 72-64.55 75.77c-43.09 4.333-79.45-29.42-79.45-71.63V126.4l-24.51 14.73C123.2 167.8 96.04 215.7 96.04 267.5L16.04 313.8c-15.25 8.751-20.63 28.38-11.75 43.63l80 138.6c8.875 15.25 28.5 20.5 43.75 11.75l103.4-59.75h136.6c35.25 0 64-28.75 64-64c26.51 0 48-21.49 48-48V288h8c13.25 0 24-10.75 24-24l.0001-48C512 202.7 501.3 191.1 488 191.1zM635.7 154.5l-79.95-138.6c-8.875-15.25-28.5-20.5-43.75-11.75l-103.4 59.75h-62.57c-37.85 0-74.93 10.61-107.1 30.63C229.7 100.4 224 110.6 224 121.6l-.0004 126.4c0 22.13 17.88 40 40 40c22.13 0 40-17.88 40-40V159.1h184c30.93 0 56 25.07 56 56v28.5l80-46.25C639.3 189.4 644.5 169.8 635.7 154.5z"
          /></svg>
        </span>
          <!--general tittle-->
          <span class="ml-2">Volunteer</span>
        </h1>

        <div class="flex mt-6 flex-1">
          <!--the gray line-->
          <div class="relative bg-gray-500 opacity-25 rounded-full w-1 left-2"></div>

          <div class="flex flex-col">

            <!--object-->
            <div class="flex py-4" v-for="info in about.volunteer">
              <!--dot-->
              <div class="z-10 flex-shrink-0 mt-5 w-3 h-3 bg-gray-900 rounded-full"></div>
              <div class="ml-8">

                <!--logo-->
                <a :href="'https://'+info.link" target="_blank">
                  <img :alt="info.organization" :src="require(`~/assets/${info.logo}`)" class="h-16 w-auto p-2">
                </a>
                <div class="mt-2">
                  <!--title-->
                  <h2 class="font-bold">{{ info.title }}</h2>
                  <!--date-->
                  <span class="text-sm font-light whitespace-no-wrap">{{ info.date }}</span>
                </div>

                <div class="text-sm">
                  <!--organization-->
                  <div class="mt-2">{{ info.organization }}</div>
                  <!--work done-->
                  <ul class="mt-2 text-xs list-disc list-inside" v-for="x in info.work">
                    <li><span v-html="x"></span></li>
                  </ul>
                </div>
              </div>
              <!--end object-->
            </div>
          </div>
        </div>
        <!--end volunteer-->
      </div>
    </Container>
  </div>
</template>

<script>
import Container from '~/components/Container'
import json from '../json/aboutData.json'

export default {
  name: 'about',
  components: {
    Container
  },
  data () {
    return {
      about: json
    }
  }
}
</script>

<style scoped>

</style>
