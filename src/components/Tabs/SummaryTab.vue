<template>
  <div class="all-coins">
    <div class="coin bitcoin">
      <div class="coin-logo" style="display: flex">
        <div class="logo"></div>
      </div>
      <div class="coin-name" style="display: flex">
        <div class="currency-symbol"></div>
        <div class="currency-name"></div>
      </div>
      <div class="coin-price"> </div>
      <div class="coin-chart">
        <Line
            id="chart-btc"
            :options="chartOptions"
            :data="chartData"
        />
      </div>
      <div style="display: flex">
        <button class="buy-sell-buttons transparent-button"> Sell </button>
        <button class="buy-sell-buttons blue-button"> Buy </button>
      </div>
    </div>
    <div class="coin ethereum">

    </div>
    <div class="coin cardano">

    </div>
    <div class="coin dogecoin">

    </div>
    <div class="coin dogecoin">

    </div>
  </div>
</template>

<script>
import { Line } from 'vue-chartjs'
import {Chart as ChartJS, CategoryScale, LinearScale, PointElement, LineElement, Title, Tooltip, Legend} from 'chart.js'

ChartJS.register(CategoryScale, LinearScale, PointElement, LineElement, Title, Tooltip, Legend)

export default {
  name: "Summary-Tab",
  components: { Line },
  data() {
    return {
      chartData: {
        labels: [],
        datasets: [{
          label: '',
          data: [15, 18, 24, 41, 56, 50, 48],
          fill: false,
          borderColor: '#7445FB',
          pointRadius: 0,
          tension: 0.3
        }]
      },
      chartOptions: {
        responsive: true,
        plugins: {
          legend: {
            display: false
          }
        }
      }
    }
  }
}
</script>

<style scoped>

.coin {
  width: 100%;
  height: 80px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-color: #FFFFFF;
  margin: 10px;
  padding: 10px;
  border: 1px solid #EBEBF3;
  border-radius: 8px;
}
.coin-chart {
  width: 148px;
  height: 60px;
}
.buy-sell-buttons {
  width: 56px;
  height: 40px;
  margin: 8px;
}
</style>
