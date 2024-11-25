<script setup>
import MainButton from "../MainButton.vue";
</script>

<template>
  <div>
    <!-- Image Section -->
    <div class="relative w-full h-96 lg:h-[70vh]">
      <img class="w-full h-full object-cover rounded-2xl" src="../../assets/img/plastic-surgery2.jpg">
      <h1 class="absolute bottom-0 bg-white text-lg sm:text-2xl md:text-3xl p-4 md:p-6 rounded-2xl left-0 right-0 mx-auto w-fit">
        {{ $t('liposuction.main.title') }}
      </h1>
    </div>

    <!-- Text Section -->
    <div class="mt-4 mx-4 md:mx-0 ">
      <p class="shadow  bg-customGray bg-opacity-70 p-6 sm:p-8 md:p-20 rounded-2xl text-sm sm:text-lg md:text-lg">
        {{ $t('liposuction.main.text') }}
      </p>
    </div>
  </div>
</template>

<style scoped>
h1:before {
  content: "";
  width: 30px;
  height: 30px;
  z-index: 100;
  background-color: transparent;
  left: -2%;
  bottom: 0;
  position: absolute;
  border-radius: 50%;
  box-shadow: 15px 15px #ffffff;
}

h1:after {
  content: "";
  width: 30px;
  height: 30px;
  background-color: transparent;
  right: -2%;
  bottom: 0;
  position: absolute;
  border-radius: 50%;
  box-shadow: -15px 15px #ffffff;
}

@media (max-width: 600px) {
  h1:before, h1:after {
    width: 0;
    height: 0;
    display: none;
  }
}
</style>
