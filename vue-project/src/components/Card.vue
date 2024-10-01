<template>
    <div class="card">
      <div class="card-header">
        <slot name="header"></slot>
      </div>
  
      <div class="card-body">
        <slot></slot>
      </div>
  
      <div class="card-footer">
        <slot name="footer"></slot>
      </div>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ddd;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    width: 100%;
    max-width: 400px;
    margin: 16px;
    background-color: #fff;
  }
  
  .card-header, .card-footer {
    padding: 16px;
    background-color: #f5f5f5;
    font-weight: bold;
  }
  
  .card-body {
    padding: 16px;
  }
  
  .card-footer {
    text-align: right;
  }
  </style>
  