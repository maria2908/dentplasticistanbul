<template>
  <div class="bg-customGray bg-opacity-70  m-4 rounded-2xl py-6">
    <h1 class="text-center text-xl md:text-2xl lg:text-3xl mb-4 ">{{ $t('main-page.standards.title') }}</h1>
    <p class="mb-12 px-4 text-sm md:text-base text-left md:text-center my-auto mx-auto lg:w-1/2 md:w-full">{{ $t('main-page.standards.subtitle') }}    </p>
    <div class="tablet mx-48 flex">
      <div class="block w-full">
        <div class="flex w-full">
          <img style="height: 30vh; " class="w-full object-cover hidden md:block lg:block" src="../../assets/img/statistic.JPG">
          <p class="text-sm md:text-base w-full bg-white text-black my-2 p-5 text-left rounded-2xl md:rounded-none md:text-center md:p-0 md:my-0 md:content-center">{{ $t('main-page.standards.text-1') }}</p>
        </div>
        <div class="flex w-full">
          <p class="text-sm md:text-base w-full bg-white text-black my-2 p-5 text-left rounded-2xl md:rounded-none md:text-center md:p-0 md:my-0 md:content-center">{{ $t('main-page.standards.text-2') }}</p>
          <img style="height: 30vh; " class=" w-full object-cover hidden md:block lg:block" src="../../assets/img/clinic.JPG">
        </div>
      </div>

      <div class="block w-full">
        <div class="flex w-full">
          <img style="height: 30vh" class="w-full object-cover hidden md:block lg:block" src="../../assets/img/our-standarts.JPG">
          <p class="text-sm md:text-base w-full bg-white text-black my-2 p-5 text-left rounded-2xl md:rounded-none md:text-center md:p-0 md:my-0 md:content-center">{{ $t('main-page.standards.text-3') }}</p>
        </div>
        <div class="flex w-full">
          <p class="text-sm md:text-base w-full bg-white text-black my-2 p-5 text-left rounded-2xl md:rounded-none md:text-center md:p-0 md:my-0 md:content-center">{{ $t('main-page.standards.text-4') }}</p>
          <img style="height: 30vh;" class="w-full object-cover hidden md:block lg:block" src="../../assets/img/our-standarts2.JPG">
        </div>
      </div>
    </div>

    <p class="text-sm md:text-base py-5 md:py-12 px-4 text-left md:text-center mx-auto lg:w-1/2 md:w-full">{{ $t('main-page.standards.subtitle-2') }}</p>
  </div>
</template>

<style scoped lang="scss">
ul {

  li {
    margin: 0 10px;
    border-radius: 15px;
    padding: 20px;
  }
}

@media (max-width: 768px) {
  .tablet {
    display: block;
    margin: 0 20px;

    p {

    }
  }
}
</style>
<script setup>
</script>