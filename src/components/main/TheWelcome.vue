<script setup>
import MainButton from "../MainButton.vue";
const scrollToFeedback = () => {
  const section = document.getElementById('feedback-section');
  if (section) {
    section.scrollIntoView({ behavior: 'smooth' });
  }
}
</script>

<template>
  <div class="flex flex-col lg:flex-row bg-customWhite p-4 sm:m-0 sm:p-0">
    <div class="relative w-full lg:w-2/3 mb-6 lg:mb-0">
      <div class="absolute bg-white p-7 logo w-32 sm:w-40">
        <img src="../../assets/img/logo.png" />
      </div>
      <img class="w-full h-72 lg:h-[93vh] object-cover rounded-2xl" src="../../assets/img/welcome-main.JPG">
    </div>
    <div class="w-full lg:w-1/3 lg:ml-12">
      <div class="bg-customDarkBeg rounded-2xl p-5 lg:mt-24 text-white">
        <h2 class="text-2xl sm:text-4xl lg:text-5xl capitalize font-semibold">
          {{ $t('main-page.welcome.title') }}
        </h2>
        <div class="flex flex-wrap justify-between mt-4 sm:mt-8 text-sm sm:text-base">
          <p>{{ $t('main-page.welcome.sub-title-1') }}</p>
          <p>{{ $t('main-page.welcome.sub-title-2') }}</p>
          <p>{{ $t('main-page.welcome.sub-title-3') }}</p>
        </div>
      </div>
      <div class="flex sm:flex-row justify-between my-8 lg:my-11 items-center px-2">
        <div class="flex mt-4 space-x-2 md:mt-0">
          <img class="w-12 h-12 rounded-3xl"
               src="https://black-pearl-storage.storage.yandexcloud.net/public/images/0ivvwt6MxwfNvLMuL8b0wlbVKW5VxMWu4hOiW90a.jpg"/>
          <img class="w-12 h-12 rounded-3xl"
               src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROSbL3Ch0JLCqu8HpTK2IPrrmc3W9jZQMXQj6FroR3qZD1JkCUBCqt9HOwOkujfYQvIgA&usqp=CAU"/>
          <img class="w-12 h-12 rounded-3xl"
               src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTi0bwzvOylBSe0mTPBljiAWPtUfysywERi6r8EvZLvYY-wSE82cGxey6AEWJCcmf9iLDA&usqp=CAU"/>
        </div>
        <button @click="scrollToFeedback" class="flex mt-4 sm:mt-0 bg-customGray p-2 rounded-2xl cursor-pointer">
          <div class="w-12 h-12 rounded-3xl text-center pt-2.5">
            <span class="material-icons text-white mt-1">visibility</span>
          </div>
          <p class="mt-3 text-white pr-3">{{ $t('main-page.welcome.feedback') }}</p>
        </button>
      </div>
      <div class="w-full gradient rounded-2xl pb-3 pt-4 px-4">
        <img class="w-full h-48 sm:h-72 object-cover mx-auto rounded-2xl" src="../../assets/img/apply.JPG"/>
        <div class="flex flex-col sm:flex-row justify-between mt-4">
          <p class="text-sm text-white rounded-2xl sm:text-base lg:w-72 sm:mr-8 mb-2">{{ $t('main-page.welcome.apply-text') }}</p>
          <MainButton class="h-fit ">{{ $t('main-page.welcome.apply') }}</MainButton>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.logo {
  border-bottom-right-radius: 30px;
}

.logo:before {
  content: "";
  width: 30px;
  height: 30px;
  background-color: transparent;
  right: -18%;
  top: 0;
  position: absolute;
  border-radius: 50%;
  box-shadow: -10px -10px #ffffff;;
}

.logo:after {
  content: "";
  width: 30px;
  height: 30px;
  background-color: transparent;
  left: 0;
  bottom: -18%;
  position: absolute;
  border-radius: 50%;
  box-shadow: -10px -10px #ffffff;;
}
</style>
