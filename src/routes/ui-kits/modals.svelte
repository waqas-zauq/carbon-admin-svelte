<script>
  import {
    Row,
    Col,
    Card,
    CardHeader,
    CardBody,
    Button,
    Modal,
    ModalHeader,
    ModalBody,
    ModalFooter
  } from "sveltestrap/src";

  let open = false;
  let size;
  const toggle = () => {
    open = !open;
    size: undefined;
  };

  const toggleLg = () => {
    size = "lg";
    open = !open;
  };
  const toggleSm = () => {
    size = "sm";
    open = !open;
  };

  let openColored = false;
  let color = "primary";
  const toggleColored = selectedColor => {
    openColored = !openColored;
    color = selectedColor;
  };

  let openFullColored = false;
  let modalColor = "primary";
  const toggleFullColored = selectedColor => {
    openFullColored = !openFullColored;
    modalColor = selectedColor;
  };
</script>

<svelte:head>
  <title>Modals</title>
</svelte:head>

<Row>
  <Col md="12">
    <Card>
      <CardHeader class="bg-light">Modals</CardHeader>

      <CardBody>
        <div class="mb-4">
          <p>Basic Modals</p>
          <Button color="primary" outline on:click={toggle}>Default</Button>
          <Button color="primary" outline on:click={toggleLg}
            >Large Modal</Button>
          <Button color="primary" outline on:click={toggleSm}
            >Small Modal</Button>
          <hr />

          <div class="my-4">
            <p>Colored Headers Modals</p>
            <Button
              color="primary"
              outline
              on:click={() => toggleColored("primary")}>Primary</Button>
            <Button
              color="success"
              outline
              on:click={() => toggleColored("success")}>Success</Button>
            <Button color="info" outline on:click={() => toggleColored("info")}
              >Info</Button>
            <Button
              color="warning"
              outline
              on:click={() => toggleColored("warning")}>Warning</Button>
            <Button
              color="danger"
              outline
              on:click={() => toggleColored("danger")}>Danger</Button>
          </div>
          <hr />

          <div class="my-4">
            <p>Full Color Modals</p>
            <Button
              color="primary"
              outline
              on:click={() => toggleFullColored("primary")}>Primary</Button>
            <Button
              color="success"
              outline
              on:click={() => toggleFullColored("success")}>Success</Button>
            <Button
              color="info"
              outline
              on:click={() => toggleFullColored("info")}>Info</Button>
            <Button
              color="warning"
              outline
              on:click={() => toggleFullColored("warning")}>Warning</Button>
            <Button
              color="danger"
              outline
              on:click={() => toggleFullColored("danger")}>Danger</Button>
          </div>
        </div></CardBody>
    </Card>
  </Col>
</Row>

<Modal isOpen={open} {toggle} {size}>
  <ModalHeader {toggle}>Modal title</ModalHeader>
  <ModalBody>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque
    lacinia non massa a euismod.
  </ModalBody>
  <ModalFooter>
    <Button color="dark" on:click={toggle}>Close</Button>
    <Button color="primary" on:click={toggle}>Save changes</Button>
  </ModalFooter>
</Modal>

<Modal isOpen={openColored} toggle={toggleColored}>
  <ModalHeader toggle={toggleColored} class="bg-{color} border-0 text-white"
    >Modal title</ModalHeader>
  <ModalBody class="p-5">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque
    lacinia non massa a euismod.
  </ModalBody>
  <ModalFooter class="border-0">
    <Button color="dark" on:click={toggleColored}>Close</Button>
    <Button {color} on:click={toggleColored}>Continue</Button>
  </ModalFooter>
</Modal>

<Modal isOpen={openFullColored} toggle={toggleFullColored}>
  <ModalHeader
    toggle={toggleFullColored}
    class="bg-{modalColor} border-0 text-white">Modal title</ModalHeader>
  <ModalBody class="bg-{modalColor} text-white p-5">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque
    lacinia non massa a euismod.
  </ModalBody>
  <ModalFooter class="bg-{modalColor} border-0">
    <Button color={modalColor} on:click={toggleFullColored}>Close</Button>
    <Button color={modalColor} on:click={toggleFullColored}>Continue</Button>
  </ModalFooter>
</Modal>

<style></style>
