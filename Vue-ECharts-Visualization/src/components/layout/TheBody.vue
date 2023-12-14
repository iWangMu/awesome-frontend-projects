<script>
  import ChartCard from '../base/ChartCard.vue';
  export default {
    components: {
      ChartCard,
    },
  };
</script>
<template>
  <section>
    <div class="chartsView">
      <ChartCard>123</ChartCard>
    </div>
    <div class="chartsView">456</div>
    <div class="chartsView">789</div>
  </section>
</template>
<style scoped>
  section {
    display: flex;
    margin-top: 5px;
    padding: 10px;
  }
  .chartsView {
    flex: 3;
  }
  .chartsView:nth-child(2) {
    flex: 5;
  }
</style>
