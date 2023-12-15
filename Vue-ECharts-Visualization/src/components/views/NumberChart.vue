<template>
  <div class="numberPanel">
    <ul class="numberList">
      <li>129876</li>
      <li>2376542</li>
    </ul>
    <ul class="descList">
      <li>前端人才数量</li>
      <li>市场需求人数</li>
    </ul>
  </div>
</template>
<style scoped>
  li {
    list-style: none;
  }
  .numberPanel {
    background-color: rgba(101, 132, 226, 0.1);
    padding: 10px;
    color: #fff;
  }
  .numberList {
    position: relative;
    height: 80px;
    line-height: 80px;
    color: #ffeb7b;
    font-family: electronicFont;
    font-size: 60px;
    text-align: center;
    border: 1px solid rgba(25, 186, 139, 0.17);
  }
  .descList {
    height: 30px;
    line-height: 30px;
    color: rgba(255, 255, 255, 0.8);
    font-size: 16px;
    text-align: center;
  }
  .numberList::before {
    position: absolute;
    top: 0;
    left: 0;
    width: 30px;
    height: 15px;
    border-left: 2px solid #02a6b5;
    border-top: 2px solid #02a6b5;
    content: '';
  }
  .numberList::after {
    position: absolute;
    bottom: 0;
    right: 0;
    width: 30px;
    height: 15px;
    border-right: 2px solid #02a6b5;
    border-bottom: 2px solid #02a6b5;
    content: '';
  }

  .numberList,
  .descList {
    display: flex;
  }
  .numberList li,
  .descList li {
    flex: 1;
    position: relative;
  }
  .numberList li:first-child::after {
    content: '';
    border: 1px solid rgba(255, 255, 255, 0.2);
    position: absolute;
    top: 25%;
    right: 0;
    height: 50%;
  }
</style>
