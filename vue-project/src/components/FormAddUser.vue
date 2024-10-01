<template>
    <div v-if="isVisible" class="modal-overlay" @click.self="closeModal">
      <div class="modal">
        <header class="modal-header">
          <slot name="header"></slot>
          <button @click="closeModal" class="modal-close">&times;</button>
        </header>
  
        <div class="modal-body">
          <form>
            <label for="name">Name</label><br>
            <input type="text" id="name" v-model="name"><br><br>
  
            <label for="email">Email</label><br>
            <input type="email" id="email" v-model="email"><br><br>
  
            <label for="address">Address</label><br>
            <input type="text" id="address" v-model="address"><br><br>
          </form>
        </div>
  
        <footer class="modal-footer">
          <slot name="footer"></slot>
        
        </footer>
      </div>
    </div>
  </template>
  
  <script setup>
import { ref } from 'vue';

  const props = defineProps({
    isVisible: {
      type: Boolean,
      default: false,
    },
  });
  
  const emit = defineEmits(['close']);
  
  const name = ref('');
  const email = ref('');
  const address = ref('');
  
  const closeModal = () => {
    emit('close');
  };
  </script>
  
  <style scoped>
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .modal {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    max-width: 200px;
    width: 100%;
  }
  
  .modal-header, .modal-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .modal-close {
    background: none;
    border: none;
    font-size: 24px;
    cursor: pointer;
  }
  
  .modal-body {
    margin: 20px 0;
  }
  </style>
  