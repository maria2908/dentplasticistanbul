<script setup>

import {onMounted} from "vue";
import MainContainer from "../layout/MainContainer.vue";
import TheMain from "../components/liposuction-dentplastistanbul/TheMain.vue";
import TheProcedure from "../components/liposuction-dentplastistanbul/TheProcedure.vue";
import TheProcedures from "../components/liposuction-dentplastistanbul/TheProcedures.vue";
import HowChoseTheClinic from "../components/liposuction-dentplastistanbul/HowChoseTheClinic.vue";
import WhyDentplastistanbul from "../components/liposuction-dentplastistanbul/WhyDentplastistanbul.vue";

onMounted(() => {
  window.scrollTo(0, 0);
});
</script>

<template>
  <main-container>
    <TheMain/>
    <div class="mx-4 md:mx-0">
      <TheProcedures/>
      <HowChoseTheClinic/>
      <TheProcedure/>
      <WhyDentplastistanbul/>
    </div>
  </main-container>
</template>
