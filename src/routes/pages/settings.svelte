<script>
  import {
    Row,
    Col,
    ListGroup,
    ListGroupItem,
    Card,
    CardHeader,
    CardBody,
    CardFooter,
    FormGroup,
    Label,
    Input,
    FormText,
    Button
  } from "sveltestrap/src";
</script>

<svelte:head>
  <title>Settings</title>
</svelte:head>

<Row>
  <Col md="2">
    <ListGroup>
      <ListGroupItem>Profile</ListGroupItem>
      <ListGroupItem active>Account Settings</ListGroupItem>
      <ListGroupItem>Notifications</ListGroupItem>
      <ListGroupItem>Subscription</ListGroupItem>
    </ListGroup>
  </Col>

  <Col md="10">
    <Card>
      <CardHeader class="bg-light">Account Settings</CardHeader>

      <CardBody>
        <Row class="mb-5">
          <Col md="4" class="mb-4">
            <div>Profile Information</div>
            <FormText>These information are visible to the public.</FormText>
          </Col>

          <Col md="8">
            <Row>
              <Col md="6">
                <FormGroup>
                  <Label for="name">Name</Label>
                  <Input id="name" />
                </FormGroup>
              </Col>

              <Col md="6">
                <FormGroup>
                  <Label for="username">Username</Label>
                  <Input id="username" />
                </FormGroup>
              </Col>
            </Row>

            <Row>
              <Col md="6">
                <FormGroup>
                  <Label for="email">Email Address</Label>
                  <Input id="email" />
                </FormGroup>
              </Col>
            </Row>

            <Row>
              <Col md="6">
                <FormGroup>
                  <Label for="website">Website Link</Label>
                  <Input id="website" />
                </FormGroup>
              </Col>
            </Row>
          </Col>
        </Row>
        <hr />

        <Row class="mt-5">
          <Col md="4" class="mb-4">
            <div>Access Credentials</div>
            <FormText
              >Leave credentials fields empty if you don't wish to change the
              password.</FormText>
          </Col>

          <Col md="8">
            <Row>
              <Col md="6">
                <FormGroup>
                  <Label for="password">Password</Label>
                  <Input id="password" type="password" />
                </FormGroup>
              </Col>

              <Col md="6">
                <FormGroup>
                  <Label for="confirmPassword">Password Confirmation</Label>
                  <Input id="confirmPassword" type="password" />
                </FormGroup>
              </Col>
            </Row>
          </Col>
        </Row>
      </CardBody>

      <CardFooter class="bg-light text-right">
        <Button type="submit" color="primary">Save Changes</Button>
      </CardFooter>
    </Card>
  </Col>
</Row>

<style></style>
