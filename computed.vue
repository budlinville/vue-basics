<script setup>
import { reactive, computed } from 'vue'

let books = ['Harry Popper', 'Series of Fortunate Events', 'Dolphins: a Tale of Extraordinary Courage'];
// books = []
const bookStr = computed(() => {
  return books.length > 0 ? books.join('... ') : "Pick up a book you ignoramus";
})
</script>

<template>
  <span>{{bookStr}}</span>
</template>