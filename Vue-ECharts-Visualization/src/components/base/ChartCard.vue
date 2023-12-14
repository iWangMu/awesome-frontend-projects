<template>
  <div class="panel">
    <slot></slot>
  </div>
</template>
<style scoped>
  .panel {
    position: relative;
    height: 320px;
    padding: 0 5px 10px 5px;
    border: 1px solid rgba(25, 186, 139, 0.17);
    margin-bottom: 10px;
    background-color: rgba(255, 255, 255, 0.03);
  }
  .panel::before {
    position: absolute;
    top: 0;
    left: 0;
    width: 15px;
    height: 15px;
    border-left: 2px solid #02a6b5;
    border-top: 2px solid #02a6b5;
    content: '';
  }
  .panel::after {
    position: absolute;
    top: 0;
    right: 0;
    width: 15px;
    height: 15px;
    border-right: 2px solid #02a6b5;
    border-top: 2px solid #02a6b5;
    content: '';
  }
</style>
