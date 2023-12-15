<template>
  <div class="map">
    <div class="earth"></div>
    <div class="map2"></div>
    <div class="map3"></div>
  </div>
</template>
<style scoped>
  .map {
    position: relative;
    height: 820px;
  }
  .earth {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 520px;
    height: 520px;
    background: url(../../static/images/map.png);
    background-size: 100% 100%;
    opacity: 0.3;
  }
  .map2 {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 640px;
    height: 640px;
    background: url(../../static/images/lbx.png);
    background-size: 100% 100%;
    opacity: 0.6;
    animation: rotate 30s linear infinite;
    z-index: 2;
  }
  .map3 {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 570px;
    height: 570px;
    background: url(../../static/images/jt.png);
    background-size: 100% 100%;
    animation: rotate1 10s linear infinite;
    opacity: 0.6;
  }
  @keyframes rotate {
    from {
      transform: translate(-50%, -50%) rotate(0deg);
    }
    to {
      transform: translate(-50%, -50%) rotate(360deg);
    }
  }
  @keyframes rotate1 {
    from {
      transform: translate(-50%, -50%) rotate(0deg);
    }
    to {
      transform: translate(-50%, -50%) rotate(-360deg);
    }
  }
</style>
