<script>
  import {
    Row,
    Col,
    Card,
    CardHeader,
    CardBody,
    CardFooter,
    FormGroup,
    Label,
    Input,
    Button
  } from "sveltestrap/src";
</script>

<svelte:head>
  <title>Login</title>
</svelte:head>

<Row class="justify-content-center">
  <Col md="5">
    <Card class="p-4">
      <CardHeader class="text-center text-uppercase h4 font-weight-light">
        Login
      </CardHeader>

      <CardBody class="py-5">
        <FormGroup>
          <Label for="email">Email</Label>
          <Input id="email" type="email" />
        </FormGroup>

        <FormGroup>
          <Label for="password">Password</Label>
          <Input id="password" type="password" />
        </FormGroup>

        <div class="custom-control custom-checkbox mt-4">
          <input type="checkbox" class="custom-control-input" id="login" />
          <label class="custom-control-label" for="login"
            >Check this custom checkbox</label>
        </div>
      </CardBody>

      <CardFooter>
        <Row>
          <Col md="6">
            <Button type="submit" color="primary" class="px-5">Login</Button>
          </Col>

          <Col md="6">
            <Button color="link">Forgot password?</Button>
          </Col>
        </Row>
      </CardFooter>
    </Card>
  </Col>
</Row>

<style></style>
