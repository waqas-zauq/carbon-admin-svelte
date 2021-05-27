<script>
  import { Row, Col, Card, CardHeader, CardBody, Alert } from "sveltestrap/src";
</script>

<svelte:head>
  <title>Alerts</title>
</svelte:head>

<Row>
  <Col md="6">
    <Card>
      <CardHeader class="bg-light">Normal Alerts</CardHeader>
      <CardBody>
        <Alert color="primary">.alert .alert-primary</Alert>
        <Alert color="secondary">.alert .alert-secondary</Alert>
        <Alert color="danger">.alert .alert-danger</Alert>
        <Alert color="success">.alert .alert-success</Alert>
        <Alert color="warning">.alert .alert-warning</Alert>
        <Alert color="info">.alert .alert-info</Alert>
      </CardBody>
    </Card>
  </Col>

  <Col md="6">
    <Card>
      <CardHeader class="bg-light">Dismissible Alerts</CardHeader>
      <CardBody>
        <Alert color="primary" dismissible
          >.alert .alert-dismissible .alert-primary</Alert>
        <Alert color="secondary" dismissible
          >.alert .alert-dismissible .alert-secondary</Alert>
        <Alert color="danger" dismissible
          >.alert .alert-dismissible .alert-danger</Alert>
        <Alert color="success" dismissible
          >.alert .alert-dismissible .alert-success</Alert>
        <Alert color="warning" dismissible
          >.alert .alert-dismissible .alert-warning</Alert>
        <Alert color="info" dismissible
          >.alert .alert-dismissible .alert-info</Alert>
      </CardBody>
    </Card>
  </Col>
</Row>

<style></style>
