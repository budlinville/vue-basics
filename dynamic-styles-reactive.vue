<script setup>
  import { reactive, computed, ref } from 'vue';
  
  // could also use refs
  // Be sure to use refVar.value inside script though... don't need ".value" in tempalte however
  // can largely use these interchangeably.. ref() uses reactive() under the hood
  const state = reactive({
    hasRedBg: false,
    hasBlueText: false
  });
  
  const toggleBg = () => state.hasRedBg = !state.hasRedBg;
  const toggleText = () => state.hasBlueText = !state.hasBlueText;
  
</script>

<template>
  <div>
    <button v-on:click="toggleBg">Red</button>
    <button @click="toggleText()">Blue</button>
    <div
      class="greenBorder"
      :class="{ redBg: state.hasRedBg, blueText: state.hasBlueText }">
      <h1>Hello!</h1>
    </div>
  </div>
</template>

<style>
  .redBg {
    background-color: red;
  }
  
  .blueText {
    color: blue;
  }
  
  .greenBorder {
    border: 5px solid green;
  }
</style>
