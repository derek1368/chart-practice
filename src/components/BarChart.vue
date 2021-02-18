<template>
  <canvas ref="barChart" id="barChart"></canvas>
</template>

<script>
import Chart from 'chart.js'

export default {
    props: ['propsdata'],

mounted() {
    var barChart = new Chart(this.$refs.barChart, {
        type: 'bar',
            data: {
            labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
            datasets: this.propsdata
        },
        options: {
            scales: {
                yAxes: [{
                    ticks: {
                        beginAtZero: true
                    }
                }]
            }
        }
    });
  }


}
</script>

<style>

</style>