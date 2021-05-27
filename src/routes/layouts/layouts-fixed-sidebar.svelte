<script>
  import { onMount, onDestroy } from "svelte";
  import {
    Row,
    Col,
    Card,
    CardHeader,
    CardBody,
    CardFooter
  } from "sveltestrap/src";

  onMount(() => {
    document.body.classList.add("sidebar-fixed");
    document.body.classList.add("header-fixed");
    var x = document.getElementsByClassName("content");
    x[0].style.height = "5000px";
  });

  onDestroy(() => {
    var x = document.getElementsByClassName("content");
    x[0].style.height = "auto";
  });
</script>

<svelte:head>
  <title>Fixed Sidebar Layout</title>
</svelte:head>

<Row>
  <Col md="4">
    <Card>
      <CardHeader>Default Card</CardHeader>
      <CardBody>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias
        architecto atque deleniti dolor dolores doloribus ducimus ea, eveniet
        facere hic illo illum laborum maiores nemo optio quas quis tenetur
        totam.
      </CardBody>
    </Card>
  </Col>

  <Col md="4">
    <Card>
      <CardHeader class="bg-light">Light Header</CardHeader>
      <CardBody>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias
        architecto atque deleniti dolor dolores doloribus ducimus ea, eveniet
        facere hic illo illum laborum maiores nemo optio quas quis tenetur
        totam.
      </CardBody>
    </Card>
  </Col>

  <Col md="4">
    <Card>
      <CardBody>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias
        architecto atque deleniti dolor dolores doloribus ducimus ea, eveniet
        facere hic illo illum laborum maiores nemo optio quas quis tenetur
        totam.
      </CardBody>
      <CardFooter class="bg-light">Card Footer</CardFooter>
    </Card>
  </Col>
</Row>

<Row class="mt-4">
  <Col md="4">
    <Card>
      <CardHeader class="bg-light">
        Card with Actions
        <div class="card-actions">
          <!-- svelte-ignore a11y-invalid-attribute -->
          <a href="javascript:void(0);" class="btn">
            <i class="fa fa-pencil-alt" />
          </a>

          <!-- svelte-ignore a11y-invalid-attribute -->
          <a href="javascript:void(0);" class="btn">
            <i class="fa fa-cog" />
          </a>
        </div>
      </CardHeader>
      <CardBody>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam
        cupiditate dolore facere magnam, rerum sint velit voluptate voluptates?
        A assumenda consequuntur debitis eaque est in ipsam iure molestiae quam.
      </CardBody>
    </Card>
  </Col>

  <Col md="4">
    <Card>
      <CardHeader class="border border-top-0 border-right-0 border-left-0">
        Card Divded Header
      </CardHeader>
      <CardBody>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam
        cupiditate dolore facere magnam, rerum sint velit voluptate voluptates?
        A assumenda consequuntur debitis eaque est in ipsam iure molestiae quam.
      </CardBody>
    </Card>
  </Col>

  <Col md="4">
    <Card>
      <CardHeader class="bg-light">Light Card</CardHeader>

      <CardBody class="bg-light">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam
        cupiditate dolore facere magnam, rerum sint velit voluptate voluptates?
        A assumenda consequuntur debitis eaque est in ipsam iure molestiae quam.
      </CardBody>
    </Card>
  </Col>
</Row>

<Row class="mt-4">
  <Col md="4">
    <Card class="text-white border-0">
      <CardHeader class="bg-primary">Primary Card</CardHeader>

      <CardBody class="bg-primary">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam
        cupiditate dolore facere magnam, rerum sint velit voluptate voluptates?
        A assumenda consequuntur debitis eaque est in ipsam iure molestiae quam.
      </CardBody>
    </Card>
  </Col>

  <Col md="4">
    <Card class="text-white border-0">
      <CardHeader class="bg-info">Info Card</CardHeader>

      <CardBody class="bg-info">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam
        cupiditate dolore facere magnam, rerum sint velit voluptate voluptates?
        A assumenda consequuntur debitis eaque est in ipsam iure molestiae quam.
      </CardBody>
    </Card>
  </Col>

  <Col md="4">
    <Card class="text-white border-0">
      <CardHeader class="bg-danger">Danger Card</CardHeader>

      <CardBody class="bg-danger">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam
        cupiditate dolore facere magnam, rerum sint velit voluptate voluptates?
        A assumenda consequuntur debitis eaque est in ipsam iure molestiae quam.
      </CardBody>
    </Card>
  </Col>
</Row>

<Row class="mt-4">
  <Col md="4">
    <Card class="text-white border-0">
      <CardHeader class="bg-success">Success Card</CardHeader>

      <CardBody class="bg-success">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam
        cupiditate dolore facere magnam, rerum sint velit voluptate voluptates?
        A assumenda consequuntur debitis eaque est in ipsam iure molestiae quam.
      </CardBody>
    </Card>
  </Col>

  <Col md="4">
    <Card class="text-white border-0">
      <CardHeader class="bg-warning">Warning Card</CardHeader>

      <CardBody class="bg-warning">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam
        cupiditate dolore facere magnam, rerum sint velit voluptate voluptates?
        A assumenda consequuntur debitis eaque est in ipsam iure molestiae quam.
      </CardBody>
    </Card>
  </Col>

  <Col md="4">
    <Card class="text-white border-0">
      <CardHeader class="bg-dark">Dark Card</CardHeader>

      <CardBody class="bg-dark">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam
        cupiditate dolore facere magnam, rerum sint velit voluptate voluptates?
        A assumenda consequuntur debitis eaque est in ipsam iure molestiae quam.
      </CardBody>
    </Card>
  </Col>
</Row>

<style></style>
