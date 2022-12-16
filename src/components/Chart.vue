<template>
  <div class="dashboard-element">
    <div class="chart">
      <div class="component-header">Summary</div>
      <div class="more-info">
        <div class="more-info-icon"></div>
      </div>
    </div>
    <Line
        id="chart-id"
        :options="chartOptions"
        :data="chartData"
    />
  </div>
</template>

<script>
import { Line } from 'vue-chartjs'
import {Chart as ChartJS, CategoryScale, LinearScale, PointElement, LineElement, Title, Tooltip, Legend} from 'chart.js'

ChartJS.register(CategoryScale, LinearScale, PointElement, LineElement, Title, Tooltip, Legend)

export default {
  name: 'Chart-component',
  components: { Line },
  data() {
    return {
      chartData: {
        labels: ['17 May', '18 May', '19 May', '20 May', '21 May', '22 May', '23 May'],
        datasets: [{
          label: 'This Month',
          data: [15, 18, 24, 41, 56, 50, 48],
          fill: false,
          borderColor: '#7445FB',
          pointRadius: 0,
          tension: 0.3
        }, {
          label: 'Last Month',
          data: [12, 30, 44, 41, 50, 56, 33],
          fill: false,
          borderColor: '#858585',
          borderDash: [10,5],
          pointRadius: 0,
          tension: 0.3
        }]
      },
      chartOptions: {
        responsive: true,
        plugins: {
          legend: {
            display: true,
            position: 'bottom',
            labels: {
              color: '#7445FB',
              usePointStyle: true,
              boxHeight: 6
            }
          }
        }
      }
    }
  }
}
</script>

<style scoped>

.chart {
  display: flex;
  justify-content: space-between;
}

</style>

