<template>
  <button @click="$emit('increment')">increment</button>
</template>

<script setup>

const emit = defineEmits(["increment"])
</script>

<style>

</style>