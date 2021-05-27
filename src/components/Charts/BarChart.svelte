<script>
  import { onMount } from "svelte";
  import Chart from "chart.js";
  import { Card, CardHeader, CardBody } from "sveltestrap/src";

  export let chartData = {
    labels: ["Red", "Blue", "Cyan", "Green", "Purple", "Orange"],
    datasets: [
      {
        label: "# of Votes",
        data: [12, 19, 3, 5, 2, 3],
        backgroundColor: [
          "rgba(244, 88, 70, 0.5)",
          "rgba(33, 150, 243, 0.5)",
          "rgba(0, 188, 212, 0.5)",
          "rgba(42, 185, 127, 0.5)",
          "rgba(156, 39, 176, 0.5)",
          "rgba(253, 178, 68, 0.5)"
        ],
        borderColor: [
          "#F45846",
          "#2196F3",
          "#00BCD4",
          "#2ab97f",
          "#9C27B0",
          "#fdb244"
        ],
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
    var ctx = document.getElementById("barChart");
    var myChart = new Chart(ctx, {
      type: "bar",
      data: chartData,
      options: chartOptions
    });
  }

  onMount(createChart);
</script>

<Card>
  <CardHeader class="bg-light">Bar Charts</CardHeader>

  <CardBody>
    <canvas id="barChart" width="100%" height="50" />
  </CardBody>
</Card>

<style></style>
