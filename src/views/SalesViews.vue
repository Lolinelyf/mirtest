<script setup>
  import { ref, onMounted } from 'vue';

  import Chart from 'chart.js/auto';

  const chart = ref();
  onMounted(() => {
    new Chart(chart.value, {
      type: 'line',

      data: {
        labels: [
          '',
          '01 Apr',
          '02 Apr',
          '03 Apr',
          '04 Apr',
          '05 Apr',
          '06 Apr',
          '07 Apr',
        ],
        datasets: [
          {
            label: '',
            data: [70, 80, 87, 79, 90, 80, 100, 150],
            fill: false,
            borderColor: 'rgb(14, 159, 110)',
            tension: 0.3,
          },
        ],
      },
      options: {
        plugins: {
          title: {
            display: true,
            text: 'Sales',
          },
          legend: false,
        },
        scales: {
          y: {
            beginAtZero: true,
          },
          x: {
            beginAtZero: true,
          },
        },
      },
    });
  });
</script>

<template>
  <div :class="$style.container">
    <canvas :class="$style.canvas" ref="chart"></canvas>
  </div>
</template>

<style module lang="scss">
  .container {
    width: 100%;
    background-color: #fff;
    border-radius: 1rem;
    margin-bottom: 1rem;
    padding: 24px;
  }
</style>
