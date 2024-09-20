<script setup>
import { ref } from 'vue'

const dataList = ref([
  'liposuction.procedures.list.text-1',
  'liposuction.procedures.list.text-2',
  'liposuction.procedures.list.text-3',
  'liposuction.procedures.list.text-4',
  'liposuction.procedures.list.text-5',
  'liposuction.procedures.list.text-6',
  'liposuction.procedures.list.text-7',
  'liposuction.procedures.list.text-8',
  'liposuction.procedures.list.text-9'
])

</script>

<template>
  <h1 class="mt-4 md:mt-12 text-xl sm:text-2xl md:text-3xl">{{ $t('liposuction.procedures.title') }}</h1>
  <p class="md:text-center md:pb-12 justify text-sm sm:text-base">{{ $t('liposuction.procedures.text') }}</p>
  <ul class="md:grid md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 w-full mx-auto md:gap-4 md:bg-customPink md:bg-opacity-80 p-4 rounded-2xl ml-6 md:ml-0">
    <li v-for="(data, index) in dataList" :key="index" class="p-1 md:p-8 md:content-center md:text-center md:text-white list-disc md:list-none">
      {{$t(data)}}
    </li>
  </ul>
</template>

<style scoped>
</style>
