<script setup>
import { ref } from "vue";
import ModalForm from '../components/ModalForm.vue'

const isModalOpened = ref(false);

const openModal = () => {
  isModalOpened.value = true;
};
const closeModal = () => {
  isModalOpened.value = false;
};

</script>

<template>
  <router-link to="#" class="hover:bg-opacity-0 hover:text-customDark border-2 items-center self-center mx-auto border-customDark content-center bg-customDark text-white px-8 py-4 rounded-3xl justify text-sm sm:text-base" @click="openModal">
    <slot></slot>
  </router-link>
  <ModalForm :isOpen="isModalOpened" @modal-close="closeModal" name="first-modal"/>
</template>
