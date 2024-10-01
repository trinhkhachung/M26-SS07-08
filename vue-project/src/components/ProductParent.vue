<template>
    <div>
     
      <ProductChildren :propName="parentData"/>
    </div>
    </template>
    
    <script setup>
    import { ref } from 'vue';
import ProductChildren from './ProductChildren.vue';
    
    const parentData=ref({
        id:1,
        name : "buoi 3 roi",
        price: "12.000d",
        quantity:10
    });
    
    </script>
    
    <style>
    
    </style>