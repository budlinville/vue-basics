<script setup>
    import { ref } from 'vue'

	const message = ref('')
    const message2 = ref('')
</script>

<template>
    <div>
        <p>{{ message }}</p>
        <textarea v-model="message" placeholder="add multiple lines" />
    
        <!-- Above is really just a simplified alias for the code below -->
        
        <p>{{ message2 }}</p>
        <textarea
            :value="message2"
            @input="e => message2 = e.target.value"
            placeholder="add multiple lines"
        />
    </div>
</template>
