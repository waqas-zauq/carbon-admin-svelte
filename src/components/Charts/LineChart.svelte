<script>
  import { onMount } from "svelte";
  import Chart from "chart.js";
  import { Card, CardHeader, CardBody } from "sveltestrap/src";

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
        backgroundColor: "rgba(66, 165, 245, 0.5)",
        borderColor: "#2196F3",
        borderWidth: 1
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
            beginAtZero: true
          }
        }
      ]
    }
  };

  function createChart() {
    var ctx = document.getElementById("lineChart");
    var myChart = new Chart(ctx, {
      type: "line",
      data: chartData,
      options: chartOptions
    });
  }

  onMount(createChart);
</script>

<Card>
  <CardHeader class="bg-light">Line Charts</CardHeader>
  <CardBody>
    <canvas id="lineChart" width="100%" height="50" />
  </CardBody>
</Card>

<style></style>
