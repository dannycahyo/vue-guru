<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)

function increment() {
  count.value++
}
function multiplyBy2() {
  count.value *= 2
}
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <h2>{{ count  }}</h2>
    <button type="button" @click="increment">count ++</button>
    <button v-if="count >= 1" type="button" @click="multiplyBy2">count * 2</button>
    <p>
      Counter component
    </p>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
