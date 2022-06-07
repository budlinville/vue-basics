<script setup>
  import {ref} from 'vue';
  
	const names= ref(["Henry", "Bob", "Jacob"]);
  
  // Vue wraps array's mutation methods s.t. they trigger view updates
  // Wrapped mutation methods are push(), pop(), shift(), unshift(), splice(), sort(), reverse()
  const addName = name => names.value.push(name);
  
  // Non-mutation methods return a new array in javascript
  // which would seem to be ineffecient in Vue as it would likely re-render the entire list
  // however, Vue is smart enough to account for this.. and its actually a pretty efficeint operation
  // Non-mutating methods include filter(), concat(), slice(), etc.
  const removeBs = () => names.value = names.value.filter(item => item[0] !== 'B')
  
  
  
</script>

<template>
	<div>
    <div :style="{border: '1px solid red', width: '5rem', margin: '1rem'}" v-for="name in names">
      {{name}}
    </div>
    <button @click="addName('Billy')">Add Billy</button>
    <button @click="removeBs('Billy')">Remove B's</button>
  </div>
</template>

<style>

</style>
