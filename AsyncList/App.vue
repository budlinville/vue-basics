<script setup>
	import {ref, onBeforeMount} from 'vue';
  
	import Users from './AsyncUserComp.vue';
  
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
