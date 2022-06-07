<script setup>
	import {ref} from 'vue';
  
  const num = ref(0);
  
</script>

<template>
  <div>
    <h1>{{num}}</h1>
        <input v-model="num"/>
    
    <!-- v-if and v-for can be used on same element, but v-if takes priority -->
    
    <div v-if="num < 10">
        <h2>Pretty small number you got there, eh?</h2>
    </div>
    <div v-else-if="num >= 10 && num < 100">
        <h2>Woah... look at you, Mr. Big Shot</h2>
    </div>
    <template v-else>
        <h2>Alright, calm down. You're freaking me out</h2>
        <h3>Feel you though</h3>
    </template>
    <!-- 
        v-show is another conditional rendering option
        difference is that v-if/else-if/else will add and remove element from DOM based on condtion
        but v-show will toggle the element's display property s.t. it is always in the DOM but
            may or may not be visible

        Rule of thumb is v-if has higher toggle costs, but v-show has higher initial render costs
            => prefer v-show to often-toggled elements and v-if if condition won't likely change at runtime
    -->
    
    <div v-show="num == 69 || num == 420">
        <p>hehe.. nice</p>
    </div>
  </div>
</template>
