<template>
  <MessageChildren @messSent="handlMess"/>
</template>

<script setup>
import MessageChildren from './MessageChildren.vue';
function handlMess(msg){
    alert(msg);
}


</script>

<style>

</style>