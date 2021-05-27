<script>
  import {
    Row,
    Col,
    Card,
    CardHeader,
    CardBody,
    Button
  } from "sveltestrap/src";
</script>

<svelte:head>
  <title>Buttons</title>
</svelte:head>

<Row>
  <Col md="12">
    <Card>
      <CardHeader class="bg-light">Buttons</CardHeader>
      <CardBody>
        <div class="mb-4">
          <p>Normal Buttons</p>
          <Button color="primary">Primary</Button>
          <Button color="secondary">Secondary</Button>
          <Button color="success">Success</Button>
          <Button color="warning">Warning</Button>
          <Button color="danger">Danger</Button>
          <Button color="info">Info</Button>
          <Button color="link">Link</Button>
        </div>
        <hr />

        <div class="my-4">
          <p>Outline Buttons</p>
          <p>Add <code>outline</code> to your buttons</p>
          <Button color="primary" outline>Primary</Button>
          <Button color="secondary" outline>Secondary</Button>
          <Button color="success" outline>Success</Button>
          <Button color="warning" outline>Warning</Button>
          <Button color="danger" outline>Danger</Button>
          <Button color="info" outline>Info</Button>
        </div>
        <hr />

        <div class="my-4">
          <p>Button Sizes</p>
          <p>
            To make different size buttons set size property to <code>sm</code>,
            <code>lg</code>
          </p>

          <Button color="secondary" size="sm">Small Size</Button>
          <Button color="secondary">Normal Size</Button>
          <Button color="secondary" size="lg">Large Size</Button>
        </div>
        <hr />

        <div class="my-4">
          <p>Button with Icons</p>
          <Button color="primary"
            ><i class="fa fa-align-center" /> &nbsp; Primary
          </Button>
          <Button color="secondary">
            <i class="fa fa-download" /> &nbsp; Secondary
          </Button>
          <Button color="success">
            <i class="fa fa-cut" />&nbsp; Success
          </Button>
          <Button color="warning">
            <i class="fa fa-clipboard" /> &nbsp; Warning
          </Button>
          <Button color="danger">
            <i class="fa fa-trash" /> &nbsp; Danger
          </Button>
        </div>
        <hr />

        <div class="my-4">
          <p>Rounded Buttons</p>
          <p>
            Add <code>.btn-rounded</code> class to your buttons to make them rounded.
          </p>
          <Button color="primary" class="btn-rounded">Primary</Button>
          <Button color="secondary" class="btn-rounded">Secondary</Button>
          <Button color="Success" class="btn-rounded">Success</Button>
          <Button color="warning" class="btn-rounded">Warning</Button>
          <Button color="danger" class="btn-rounded">Danger</Button>
          <Button color="info" class="btn-rounded">Info</Button>
        </div>
        <hr />

        <div class="my-4">
          <p>Block Buttons</p>
          <p>
            Add <code>.btn-block</code> class to your buttons to make them full width.
          </p>
          <Button color="primary" class="btn-block">Primary</Button>
          <Button color="secondary" class="btn-block">Secondary</Button>
          <Button color="success" class="btn-block">Success</Button>
          <Button color="warning" class="btn-block">Warning</Button>
          <Button color="danger" class="btn-block">Danger</Button>
          <Button color="info" class="btn-block">Info</Button>
        </div>
      </CardBody>
    </Card>
  </Col>
</Row>

<style></style>
