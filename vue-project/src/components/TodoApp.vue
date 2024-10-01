<template>
    <div>
        <h1>id to delete:{{idD}}</h1>
      <TodoItem @delete="handlchange"/>

 
  </div>
  </template>
  
  <script setup>
import { ref } from 'vue';
import TodoItem from './TodoItem.vue';
const idD = ref('')
const handlchange = (id) => idD.value=id;
   
  </script>
  
  <style>
  
  </style>