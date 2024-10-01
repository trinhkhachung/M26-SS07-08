<template>
  <button @click="$emit('messSent','welcome to Rekkei Academy')">sent mess</button>
</template>

<script setup>
const emit = defineEmits(['messSent'])
</script>

<style>

</style>