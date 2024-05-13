<template>
  <div class="container">
    <div class="col-6">
      <div class="card">
        <div class="card-header">
          <div class="card-title">
            <h1 class="title">Recent Workflow</h1>
          </div>
        </div>
        <div class="card-body">
          <Bar
              id="my-chart-id2"
              :options="chartOptions"
              :data="chartData"
          />
        </div>
        <div class="card-footer text-green font-size-12">
          <span class="mr-5 material-symbols-outlined ">trending_up</span>
          <span class="mr-5">12 %</span>
        </div>
      </div>
    </div>


    <div class="col-6">
      <div class="card">
        <div class="card-header">
          <div class="card-title">
            <h1 class="title">Recent Marketing</h1>
          </div>
        </div>
        <div class="card-body">
          <Bar
              id="my-chart-id"
              :options="chartOptions"
              :data="chartData"
          />
        </div>
        <div class="card-footer text-green font-size-12">
          <span class="mr-5 material-symbols-outlined ">trending_up</span>
          <span class="mr-5"> 21 %</span>
        </div>
      </div>
    </div>


  </div>
</template>

<script>

import { Bar } from 'vue-chartjs';
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale);
export default {
  name: "TheCard",
  components: {
    Bar,
  },
  data: function () {
    return {
      chartData: {
        labels: [
          'January',
          'February',
          'March',
          'April',
          'May',
          'June',
          'July'
        ],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [40, 39, 10, 40, 39, 80, 40]
          }
        ]
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false
      }
    }
  },
  mounted() {
  },
  methods:{

  }

}
</script>

<style scoped>

</style>