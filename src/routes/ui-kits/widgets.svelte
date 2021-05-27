<script>
  import { Row, Col } from "sveltestrap/src";

  import SummaryCard from "../../components/SummaryCard.svelte";
  import ProgressCard from "../../components/ProgressCard.svelte";
  import ChartCard from "../../components/ChartCard.svelte";
</script>

<svelte:head>
  <title>Widgets</title>
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
  <Col md="3">
    <ProgressCard
      cardValue="32s"
      cardText="Avg. Response Time"
      cardProgressBarValue="35"
      cardProgressBarColor="warning" />
  </Col>

  <Col md="3">
    <ProgressCard
      cardValue="565"
      cardText="Total Downloads"
      cardProgressBarValue="24"
      cardProgressBarColor="success" />
  </Col>

  <Col md="3">
    <ProgressCard
      cardValue="232"
      cardText="New Users"
      cardProgressBarValue="65"
      cardProgressBarColor="info" />
  </Col>

  <Col md="3">
    <ProgressCard
      cardValue="$44,000"
      cardText="Income"
      cardProgressBarValue="70"
      cardProgressBarColor="dark" />
  </Col>
</Row>

<Row>
  <Col md="3">
    <ChartCard />
  </Col>

  <Col md="3">
    <ChartCard backgroundColor="primary" />
  </Col>

  <Col md="3">
    <ChartCard backgroundColor="success" />
  </Col>

  <Col md="3">
    <ChartCard backgroundColor="dark" />
  </Col>
</Row>

<style></style>
