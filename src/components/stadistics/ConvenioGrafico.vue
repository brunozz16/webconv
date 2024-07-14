<template>
  <div class="chart-container">
    <div ref="chartContainer" class="chart"></div>
  </div>
</template>

<script>
import { createChart } from "lightweight-charts";

export default {
  data() {
    return {
      chartData: [
        { time: '2019-04-11', value: 80.01 },
        { time: '2019-05-12', value: 96.63 },
        { time: '2019-06-12', value: 104.63 },
        { time: '2019-07-12', value: 124.63 }
        // ... el resto de tus datos
      ],
      chart: null,
    };
  },
  mounted() {
    this.createChart();
    window.addEventListener('resize', this.resizeChart);
  },
  beforeUnmount() {
    window.removeEventListener('resize', this.resizeChart);
  },
  methods: {
    createChart() {
      const chartContainer = this.$refs.chartContainer;
      this.chart = createChart(chartContainer, { width: chartContainer.clientWidth, height: chartContainer.clientHeight });
      const lineSeries = this.chart.addLineSeries();
      lineSeries.setData(this.chartData);
    },
    resizeChart() {
      const chartContainer = this.$refs.chartContainer;
      if (this.chart) {
        this.chart.resize(chartContainer.clientWidth, chartContainer.clientHeight);
      }
    }
  },
};
</script>

<style scoped>
.chart-container {
  width: 100%;
  height: 100vh; /* o 100% si el contenedor padre tiene una altura definida */
}

.chart {
  width: 50%; /* Asegúrate de que ocupe todo el ancho disponible */
  height: 50%;
  border: 5px solid black;
}
</style>
