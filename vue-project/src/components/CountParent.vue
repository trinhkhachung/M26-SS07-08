<template>
  <div>
    <CountChildren @increment="handlchange"/>
    <h1>count: {{count}}</h1>
</div>
</template>

<script setup>
import { ref } from 'vue';
import CountChildren from './CountChildren.vue';
const count = ref(0);
const handlchange = () => count.value++;


</script>

<style>

</style>