<script setup>
import { ref } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

const slides = ref([
  {
    title: 'main-page.services.slider.title-1',
    img: 'https://www.centerplast.de/wp-content/uploads/2024/02/behandlung-zum-facelifting.jpg',
    text: ' 3400€'
  },
  {
    title: 'main-page.services.slider.title-2',
    img: 'https://www.klmedestet.ru/wp-content/uploads/2017/05/mammo-2.jpg',
    text: ' > 2600€'
  },
  {
    title: 'main-page.services.slider.title-3',
    img: 'https://hrytsevychclinic.com/storage/cache/17101672635409-307x350.webp',
    text: ' 2500€'
  },
  {
    title: 'main-page.services.slider.title-4',
    img: 'https://kim-rm.ru/assets/img/uslugi/%D0%9F%D0%BB%D0%B0%D1%81%D1%82%D0%B8%D0%BA%D0%B0%20%D1%82%D0%B5%D0%BB%D0%B0.jpg',
    text: ' > 2600€'
  },
  {
    title: 'main-page.services.slider.title-5',
    img: 'https://stomaservice.com.ua/storage/cache/16552003465423-430x430.webp',
    text: ' 250€'
  },
  {
    title: 'main-page.services.slider.title-6',
    img: 'https://kredo-dent.ru/wp-content/uploads/2024/07/viniry-2-427x388.jpg',
    text: ' 140€'

  },
  {
    title: 'main-page.services.slider.title-7',
    img: 'https://fortuna-dent.com.ua/images/1493107285_gollivudskie-viniry.JPG',
    text: ' 250€'

  },
])

const settings = ref({
  itemsToShow: 1,
  snapAlign: 'center',
})

const breakpoints = ref({
  640: {
    itemsToShow: 1,
    snapAlign: 'center',
  },
  768: {
    itemsToShow: 2,
    snapAlign: 'center',
  },
  1024: {
    itemsToShow: 3,
    snapAlign: 'start',
  },
  1440: {
    itemsToShow: 4,
    snapAlign: 'start',
  },
})
</script>


<template>
  <h1 class="text-center text-xl md:text-2xl lg:text-3xl mb-0 md:mb-4">{{ $t('main-page.services.title') }}</h1>
  <div class="flex flex-col lg:flex-row gap-8 items-center md:items-start">
    <!-- Text section that will adapt flexibly -->
    <div class="w-full lg:w-1/3 p-6 rounded-2xl h-auto text-left bg-gray-100 text-sm md:text-base">
      <p>{{ $t('main-page.services.text-1') }}</p>
      <p class="mt-8 md:mt-16">{{ $t('main-page.services.text-2') }}</p>
    </div>

    <!-- Carousel section that will be flexible on all devices -->
    <div class="w-full lg:w-2/3 carousel-dent mb-10">
      <Carousel v-bind="settings" :breakpoints="breakpoints" class="w-full">
        <Slide v-for="slide in slides" :key="slide.title" class="p-4">
          <div class="carousel__item mx-auto text-center w-[300px]">
            <img :src="slide.img" class="h-72 mx-auto w-full  object-cover max-w-xs rounded-xl shadow-lg" />
            <p class="w-full mt-4 text-justify text-sm md:text-base">{{$t(slide.title)}}</p>
            <div class="flex mt-2 bg-customPink p-5 rounded-2xl bg-opacity-50">
              <span class="font-bold">{{$t('main-page.services.cost')}}: </span>&nbsp;
              <span> {{$t(slide.text)}}</span>
            </div>
          </div>
        </Slide>

        <template #addons>
          <div class="navi-services">
            <Navigation />
          </div>
        </template>
      </Carousel>
    </div>
  </div>
</template>

<style lang="scss">
.carousel__slide {
  align-items: start;
  justify-content: center;
}
.navi-services {
  margin-top: 10px;

  .carousel__next {
    margin-left: 60px;
  }
  .carousel__prev,
  .carousel__next {
    margin-top: 20px;
    position: absolute;
    color: white;
    padding: 5px;
    background-color: #AD9173;
    border-radius: 40px;
    left: 0%;
    top: 100%;
  }
}

@media (max-width: 800px){
  .carousel-dent {
    .carousel__prev,
    .carousel__next {
      top: -7% !important;
      left: 75% !important;
    }
  }

}

</style>
