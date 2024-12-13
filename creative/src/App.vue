<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
const config = {
  itemsToShow: 1,
  wrapAround: true,
  autoplay: 3000,
}
</script>

<template>
  <body>
    <div>
      <Carousel v-bind="config">
        <Slide v-for="slide in 1" :key="slide">
          <div class="carousel__item">
            <img
              src="https://elements-resized.envatousercontent.com/elements-cover-images/369775a9-ea89-44f5-aca1-4a3c4e3b4e4d?w=433&cf_fit=scale-down&q=85&format=auto&s=9f3b00f7ec57cbe4fb9859313c8ca6c02f8b8907a0e286a07e3466f7a44965ec"
            />
          </div>
        </Slide>
      </Carousel>
    </div>
  </body>
</template>

<style lang="scss" scoped>
header {
  line-height: 1.5;
}

body {
  display: block;

  img {
    width: 100%;
  }
}
</style>
