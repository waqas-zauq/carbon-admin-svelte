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
        backgroundColor: [
          "rgba(244, 88, 70, 0.5)",
          "rgba(33, 150, 243, 0.5)",
          "rgba(0, 188, 212, 0.5)",
          "rgba(42, 185, 127, 0.5)",
          "rgba(156, 39, 176, 0.5)",
          "rgba(253, 178, 68, 0.5)"
        ],
        borderColor: [
          "rgba(244, 88, 70, 0.5)",
          "rgba(33, 150, 243, 0.5)",
          "rgba(0, 188, 212, 0.5)",
          "rgba(42, 185, 127, 0.5)",
          "rgba(156, 39, 176, 0.5)",
          "rgba(253, 178, 68, 0.5)"
        ],
        borderWidth: 1
      }
    ]
  };

  export let chartOptions = {};

  function createChart() {
    var ctx = document.getElementById("pieChart");
    var myChart = new Chart(ctx, {
      type: "pie",
      data: chartData,
      options: chartOptions
    });
  }

  onMount(createChart);
</script>

<Card>
  <CardHeader class="bg-light">Pie Chart</CardHeader>

  <CardBody>
    <canvas id="pieChart" width="100%" height="50" />
  </CardBody>
</Card>

<style></style>
