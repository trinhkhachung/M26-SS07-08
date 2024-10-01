<template>
  <div>
    <h1>Bài 1</h1>
    <ParentComponent/>

    <h1>Bài 2</h1>
    <ProductParent/>

    <h1>Bài 3</h1>
    <CountParent/>

    <h1>Bài 4</h1>
    <TodoApp/>

    <h1>Bài 5</h1>
    <div>
      <button @click="openModal">Mở Modal</button>

      <Modal :isVisible="isModalVisible" @close="closeModal">
        <template #header>
          <h2>Thông báo từ hệ thống</h2>
        </template>
        
        <p>Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào nút 'Close'.</p>
        
        <template #footer>
          <button @click="closeModal">Close</button>
        </template>
      </Modal>
    </div>
    <h1>bai 6</h1>
    <div>
      <Card>
        <template #header>
          Thông tin sản phẩm
        </template>
  
        Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi bật và giá cả hợp lý.
        <template #footer>
          <button @click="viewDetails">Xem chi tiết</button>
        </template>
      </Card>
    </div>
    <h1>bai 7</h1>
    <MessageParent/>
    <h1>bai 8</h1>
    <ListUser/>
    
  </div>
</template>

<script setup>
import { ref } from 'vue';

import CountParent from './components/CountParent.vue';
import ParentComponent from './components/ParentComponent.vue';
import ProductParent from './components/ProductParent.vue';
import TodoApp from './components/TodoApp.vue';
import Modal from './components/Modal.vue'; 

const isModalVisible = ref(false);

const openModal = () => {
  isModalVisible.value = true;
};

const closeModal = () => {
  isModalVisible.value = false;
};
import Card from './components/Card.vue';
import MessageParent from './components/MessageParent.vue';
import ListUser from './components/ListUser.vue';


const viewDetails = () => {
  alert('Xem chi tiết sản phẩm!');
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
.btn{
  display: flex;
  gap: 20px;
}
</style>
