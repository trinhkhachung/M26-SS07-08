<template>
<div>
  <h1>Parent: {{parentData}}</h1>
  <ChildrenComponent :propName="parentData"/>
</div>
</template>

<script setup>
import { ref } from 'vue';
import ChildrenComponent from './ChildrenComponent.vue';
const parentData=ref("rikkei academy");

</script>

<style>

</style>