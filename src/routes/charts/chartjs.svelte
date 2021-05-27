<script>
  import { Row, Col } from "sveltestrap/src";

  import {
    BarChart,
    LineChart,
    RadarChart,
    PieChart
  } from "../../components/Charts";
</script>

<svelte:head>
  <title>Chart.js</title>
</svelte:head>

<Row>
  <Col md="6">
    <BarChart />
  </Col>

  <Col md="6">
    <LineChart />
  </Col>
</Row>

<Row class="mt-4">
  <Col md="6">
    <RadarChart />
  </Col>

  <Col md="6">
    <PieChart />
  </Col>
</Row>

<style></style>
