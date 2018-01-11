<template>
  <div class="box">
    <v-chart :force-fit="true" :height="height" :data="data" class="chart">
      <v-tooltip />
      <v-axis />
      <v-legend />
      <v-bar :position="'time*waiting'"/>
      <v-line :position="'time*people'"/>
    </v-chart>
  </div>
</template>

<script>
  const data = [
    { time: '10:10', waiting: 2, people: 2 },
    { time: '10:15', waiting: 6, people: 3 },
    { time: '10:20', waiting: 2, people: 5 },
    { time: '10:25', waiting: 9, people: 1 },
    { time: '10:30', waiting: 2, people: 3 },
    { time: '10:35', waiting: 2, people: 1 },
    { time: '10:40', waiting: 1, people: 2 }
  ]

  export default {
    data() {
      return {
        data,
        height: 400
      };
    }
  };
</script>


<style>
  * {
    margin: 0;
    padding: 0;
  }
  html, body, .box{
    height: 100%;
  }
  .chart {
    height: 400px;
    width: 100%;
    margin-top: -200px;
    position:absolute;
    top: 50%;

  }
</style>