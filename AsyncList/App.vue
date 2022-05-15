<script setup>
	import {ref, onBeforeMount} from 'vue';
  
	import Users from './async-user-comp.vue';
  
</script>

<template>
    <Suspense>
  	    <template #default>
    	    <Users />
        </template>
        <template #fallback>
            <div>
                Loading...
            </div>
        </template>
    </Suspense>
</template>

<style>

  
</style>
