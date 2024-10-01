<!-- ListUser.vue -->
<template>
    <div>
      <button @click="openModal">Add user</button>
  
      <FormAddUser :isVisible="isModalVisible" @close="closeModal">
        <template #header>
          <h2>Form Add User</h2>
        </template>
  
        <template #footer>
          <button @click="closeModal">Close</button>
        </template>
      </FormAddUser>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import FormAddUser from './FormAddUser.vue';
  
  const isModalVisible = ref(false);
  
  // Mở form modal
  const openModal = () => {
    isModalVisible.value = true;
  };
  
  // Đóng form modal
  const closeModal = () => {
    isModalVisible.value = false;
  };
  </script>
  
  <style scoped>
  button {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    border: none;
    cursor: pointer;
    border-radius: 4px;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  </style>
  