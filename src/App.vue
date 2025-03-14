<script setup>
import {onMounted} from 'vue';
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import SEO from './components/SEO.vue'

onMounted(() => {
  window.scrollTo(0, 0);
});
localStorage.setItem('locale', 'ru');

</script>

<template>
  <SEO />
  <the-header></the-header>
  <router-view></router-view>
  <the-footer></the-footer>
</template>


<style scoped>
</style>