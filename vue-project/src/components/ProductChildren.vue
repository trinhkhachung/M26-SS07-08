<template>
    <div><h1>du lieu trong compoment con </h1>
        <p> {{props.propName}}</p>
      
    </div>
    
  </template>
  
  <script setup>
  const props = defineProps(['propName'])
  </script>
  
  <style>
  
  </style>