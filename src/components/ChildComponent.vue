<script setup>
import { ref } from "vue";

const show = ref(true);

defineExpose({ show });
</script>

<template>
    <button @click="show = !show">Open Section in component</button>
    <Transition>
      <div class="board" v-if="show" ref="board"></div>
    </Transition>
</template>

<style>
.board {
  width: 90%;
  height: 40px;
  background-color: darkgray;
  border-radius: 4px;
}

.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
