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
  <title>Register</title>
</svelte:head>

<Row class="justify-content-center">
  <Col md="5">
    <Card class="p-4">
      <CardHeader class="text-center text-uppercase h4 font-weight-light">
        Register
      </CardHeader>

      <CardBody class="py-5">
        <FormGroup>
          <Label for="name">Name</Label>
          <Input id="name" />
        </FormGroup>

        <FormGroup>
          <Label for="email">Email</Label>
          <Input id="email" type="email" />
        </FormGroup>

        <FormGroup>
          <Label for="password">Password</Label>
          <Input id="password" type="password" />
        </FormGroup>

        <FormGroup>
          <Label for="confirmPassword">Confirm Password</Label>
          <Input id="confirmPassword" type="password" />
        </FormGroup>
      </CardBody>

      <CardFooter>
        <Button type="submit" color="success" block>Create Account</Button>
      </CardFooter>
    </Card>
  </Col>
</Row>

<style></style>
