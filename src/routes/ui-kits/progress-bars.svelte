<script>
  import {
    Row,
    Col,
    CardDeck,
    Card,
    CardHeader,
    CardBody,
    Progress
  } from "sveltestrap/src";
</script>

<svelte:head>
  <title>Progress Bars</title>
</svelte:head>

<Row>
  <Col md="12">
    <CardDeck>
      <Card>
        <CardHeader class="bg-light">Normal Progress Bars</CardHeader>
        <CardBody>
          <Progress />
          <Progress class="mt-3" value="25" />
          <Progress class="mt-3" value="35" color="success" />
          <Progress class="mt-3" value="55" color="danger" />
          <Progress class="mt-3" value="25" color="warning" />
          <Progress class="mt-3" value="65" color="info" />
          <Progress class="mt-3" value="30" color="secondary" />
        </CardBody>
      </Card>

      <Card>
        <CardHeader class="bg-light">Stripped Progress Bars</CardHeader>

        <CardBody>
          <Progress class="mt-3" value="25" striped />
          <Progress class="mt-3" value="35" color="success" striped />
          <Progress class="mt-3" value="55" color="danger" striped />
          <Progress class="mt-3" value="25" color="warning" striped />
          <Progress class="mt-3" value="65" color="info" striped />
          <Progress class="mt-3" value="30" color="secondary" striped />
        </CardBody>
      </Card>
    </CardDeck>
  </Col>
</Row>

<Row class="mt-4">
  <Col md="12">
    <CardDeck>
      <Card>
        <CardHeader class="bg-light">Progress Bar Sizes</CardHeader>

        <CardBody>
          <Progress value="25" style="height: 1px" />
          <Progress
            class="mt-3"
            value="35"
            style="height: 10px"
            color="success" />
          <Progress
            class="mt-3"
            value="55"
            style="height: 20px"
            color="danger" />
          <Progress
            class="mt-3"
            value="25"
            style="height: 30px"
            color="warning" />
          <Progress class="mt-3" value="65" style="height: 40px" color="info" />
          <Progress
            class="mt-3"
            value="30"
            style="height: 50px"
            color="secondary" />
        </CardBody>
      </Card>

      <Card>
        <CardHeader class="bg-light">Labels with Progress Bars</CardHeader>

        <CardBody>
          <Progress />
          <Progress class="mt-3" value="25" />
          <Progress class="mt-3" value="35" color="success">35%</Progress>
          <Progress class="mt-3" value="55" color="danger">55%</Progress>
          <Progress class="mt-3" value="25" color="warning">25%</Progress>
          <Progress class="mt-3" value="65" color="info">65%</Progress>
          <Progress class="mt-3" value="30" color="secondary">30%</Progress>
        </CardBody>
      </Card>
    </CardDeck>
  </Col>
</Row>

<style></style>
