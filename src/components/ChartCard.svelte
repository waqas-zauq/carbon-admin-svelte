<script>
  import { onMount } from "svelte";
  import Chart from "chart.js";
  import { Card, CardBody } from "sveltestrap/src";

  export let totalTraffic = "120,124";
  export let todayTraffic = "+2,452 (55%)";
  export let backgroundColor = "danger";

  export let chartData = {
    labels: [
      "Jan",
      "Feb",
      "Mar",
      "Apr",
      "May",
      "Jun",
      "Jul",
      "Aug",
      "Sep",
      "Oct",
      "Nov",
      "Dec"
    ],
    datasets: [
      {
        label: "Users",
        data: [12, 19, 3, 5, 2, 3, 20, 33, 23, 12, 33, 10],
        borderColor: "#fff",
        borderWidth: 1,
        fill: false
      }
    ]
  };

  export let chartOptions = {
    legend: {
      display: false
    },
    scales: {
      yAxes: [
        {
          ticks: {
            beginAtZero: true,
            display: false
          },
          gridLines: {
            display: false,
            drawBorder: false
          }
        }
      ],
      xAxes: [
        {
          ticks: {
            display: false
          },
          gridLines: {
            display: false,
            drawBorder: false
          }
        }
      ]
    }
  };

  function createChart() {
    var ctx = document.getElementById(`${backgroundColor}LineChart`);
    var myChart = new Chart(ctx, {
      type: "line",
      data: chartData,
      options: chartOptions
    });
  }

  onMount(createChart);
</script>

<Card class="bg-{backgroundColor} border-0">
  <CardBody class="d-flex justify-content-between text-white flex-column">
    <div class="font-weight-bold">
      <span>Traffic</span>
      <span class="float-right">{totalTraffic}</span>
    </div>

    <div class="small mb-3">
      <span>Today</span>
      <span class="float-right">{todayTraffic}</span>
    </div>

    <canvas id="{backgroundColor}LineChart" width="100%" height="30" />
  </CardBody>
</Card>

<style></style>
