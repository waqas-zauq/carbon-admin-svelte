<script>
  import { onMount } from "svelte";
  import Chart from "chart.js";
  import { Row, Col, Card, CardHeader, CardBody } from "sveltestrap/src";
  import SummaryCard from "../components/SummaryCard.svelte";

  let chartData = {
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

  let chartOptions = {
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

<svelte:head>
  <title>Dashboard</title>
</svelte:head>

<Row>
  <Col md="3">
    <SummaryCard cardValue="54" cardText="Total Users" cardIcon="people" />
  </Col>

  <Col md="3">
    <SummaryCard cardValue="$32,400" cardText="Income" cardIcon="wallet" />
  </Col>

  <Col md="3">
    <SummaryCard
      cardValue="900"
      cardText="Downloads"
      cardIcon="cloud-download" />
  </Col>

  <Col md="3">
    <SummaryCard cardValue="32s" cardText="Time" cardIcon="clock" />
  </Col>
</Row>

<Row>
  <Col md="12">
    <Card>
      <CardHeader>Total Users</CardHeader>

      <CardBody class="p-0">
        <div class="p-4">
          <canvas id="lineChart" width="100%" height="20" />
        </div>

        <div
          class="justify-content-around mt-4 p-4 bg-light d-flex border-top d-md-down-none">
          <div class="text-center">
            <div class="text-muted small">Total Traffic</div>
            <div>12,457 Users (40%)</div>
          </div>

          <div class="text-center">
            <div class="text-muted small">Banned Users</div>
            <div>95,333 Users (5%)</div>
          </div>

          <div class="text-center">
            <div class="text-muted small">Page Views</div>
            <div>957,565 Pages (50%)</div>
          </div>

          <div class="text-center">
            <div class="text-muted small">Total Downloads</div>
            <div>957,565 Files (100 TB)</div>
          </div>
        </div>
      </CardBody>
    </Card>
  </Col>
</Row>

<style>
</style>
