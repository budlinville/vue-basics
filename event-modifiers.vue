<script setup>
  const _alert = str => alert(str);
</script>

<template>
    <!-- 'exact' makes sure that only that key is pressed -->
	<input
		@keyup.up.exact="_alert('UP')"
        @keyup.down.exact="_alert('DOWN')"
        @keyup.left="_alert('LEFT')"
        @keyup.right="_alert('RIGHT')"
    />
</template>
