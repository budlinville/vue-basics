<script setup>
	import {ref} from 'vue';
  
  const getUsers = async n => {
    const res = await fetch(`https://randomuser.me/api/?results=${n}`);
    return await res.json();
  }
  
    const res = await getUsers(3);
    const users = res.results;
</script>

<template>
  <div id="container">
    <div class="card" v-for="({cell, gender, email, picture, name}, i) in users">
      <div class='line1'>
        <img class="img" :src="picture.medium" alt="#N/A">
      	<h1>{{`${name.first} ${name.last} (${i})`}}</h1>
      </div>
      <h3>{{email}}</h3>
      <h3>{{cell}}</h3>
      <p>{{gender}}</p>
    </div>
  </div>
</template>

<style>
  #container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: space-around;
  }
  
  .card {
    border: 1px solid black;
    border-radius: 15px;
    margin: 1rem;
    padding: 1rem;
  }
  
  .img {
    border-radius: 20px;
    margin-right: 2rem
  }
  
  .line1 {
    display: flex;
  }
  
</style>
