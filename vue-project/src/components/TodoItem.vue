<template>
    <button @click="$emit('delete','1')">delete</button>
  </template>
  
  <script setup>
  
  const emit = defineEmits(["delete"])
  </script>
  
  <style>
  
  </style>