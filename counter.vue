<script setup>
import { ref } from 'vue'

const count = ref(1)
</script>

<template>
  <h1>{{ count }}</h1>
  <input v-model.number="count">
  <button @click="count+=5">+5</button>
</template>