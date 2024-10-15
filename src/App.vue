<script setup>
import { ref } from "vue";
import ChildComponent from "./components/ChildComponent.vue";

const childComponent = ref();
</script>

<template>
  <button @click="childComponent.show = !childComponent.show">
    Open section in parent
  </button>
  <ChildComponent ref="childComponent"></ChildComponent>
</template>

<style scoped></style>
