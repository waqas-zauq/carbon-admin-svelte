<script>
  import { onMount } from "svelte";
  import Chart from "chart.js";
  import { Card, CardHeader, CardBody } from "sveltestrap/src";

  export let chartData = {
    labels: ["Red", "Blue", "Cyan", "Green", "Purple", "Orange"],
    datasets: [
      {
        label: "Users",
        data: [100, 45, 87, 50, 77, 20],
        backgroundColor: "rgba(244, 88, 70, 0.5)",
        borderColor: "#F45846",
        borderWidth: 1
      },
      {
        label: "Votes",
        data: [23, 55, 75, 54, 95, 100],
        backgroundColor: "rgba(33, 150, 243, 0.5)",
        borderColor: "#2196F3",
        borderWidth: 1
      }
    ]
  };

  export let chartOptions = {};

  function createChart() {
    var ctx = document.getElementById("radarChart");
    var myChart = new Chart(ctx, {
      type: "radar",
      data: chartData,
      options: chartOptions
    });
  }

  onMount(createChart);
</script>

<Card>
  <CardHeader class="bg-light">Radar Chart</CardHeader>

  <CardBody>
    <canvas id="radarChart" width="100%" height="50" />
  </CardBody>
</Card>

<style></style>
