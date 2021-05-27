<script>
  import {
    Row,
    Col,
    Card,
    CardHeader,
    CardBody,
    FormGroup,
    Label,
    Input,
    FormText,
    InputGroup,
    InputGroupAddon,
    InputGroupText,
    Button,
    ButtonDropdown,
    DropdownItem,
    DropdownMenu,
    DropdownToggle
  } from "sveltestrap/src";
</script>

<svelte:head>
  <title>Forms</title>
</svelte:head>

<Row>
  <Col md="12">
    <Card>
      <CardHeader class="bg-light">Basic Forms</CardHeader>

      <CardBody>
        <Row>
          <Col md="4">
            <FormGroup>
              <Label for="normal-input" class="form-control-label"
                >Normal Input</Label>
              <Input id="normal-input" placeholder="Input value" />
            </FormGroup>
          </Col>

          <Col md="4">
            <FormGroup>
              <Label for="read-only" class="form-control-label"
                >Read Only</Label>
              <Input id="read-only" placeholder="Input value" readonly />
            </FormGroup>
          </Col>

          <Col md="4">
            <FormGroup>
              <Label for="disabled-input" class="form-control-label"
                >Disabled Input</Label>
              <Input id="disabled-input" placeholder="Input value" disabled />
            </FormGroup>
          </Col>
        </Row>

        <Row class="mt-4">
          <Col md="4">
            <FormGroup>
              <Label for="placeholder-input" class="form-control-label"
                >Placeholder</Label>
              <Input id="placeholder-input" placeholder="Placeholder text" />
            </FormGroup>
          </Col>

          <Col md="4">
            <FormGroup>
              <Label for="required-input" class="require">Required</Label>
              <Input id="required-input" placeholder="Input value" />
            </FormGroup>
          </Col>

          <Col md="4">
            <FormGroup>
              <Label class="form-control-label">Static</Label>
              <p class="form-control-plaintext">email@example.com</p>
            </FormGroup>
          </Col>
        </Row>

        <Row class="mt-4">
          <Col md="4">
            <FormGroup>
              <Label for="help-text-input" class="form-control-label"
                >Help text</Label>
              <Input id="help-text-input" placeholder="Enter email" />
              <FormText
                >We'll never share your email with anyone else.</FormText>
            </FormGroup>
          </Col>
        </Row>

        <Row class="mt-4">
          <Col md="4">
            <Label>Sizes</Label>

            <FormGroup>
              <Input placeholder="Small" bsSize="sm" />
            </FormGroup>

            <FormGroup>
              <Input placeholder="Normal" />
            </FormGroup>

            <FormGroup>
              <Input placeholder="Large" bsSize="lg" />
            </FormGroup>
          </Col>

          <Col md="4">
            <FormGroup>
              <Label for="single-select">Example select</Label>
              <Input type="select" id="single-select" name="select">
                <option>1</option>
                <option>2</option>
                <option>3</option>
                <option>4</option>
                <option>5</option>
              </Input>
            </FormGroup>

            <FormGroup>
              <Label for="multi-select">Example multiple select</Label>
              <Input
                type="select"
                id="multi-select"
                name="selectMulti"
                multiple="">
                <option>1</option>
                <option>2</option>
                <option>3</option>
                <option>4</option>
                <option>5</option>
              </Input>
            </FormGroup>
          </Col>

          <Col md="4">
            <FormGroup>
              <Label for="textarea">Example textarea</Label>
              <Input type="textarea" id="textarea" rows="6" />
            </FormGroup>
          </Col>
        </Row>
      </CardBody>
    </Card>
  </Col>
</Row>

<Row class="mt-4">
  <Col md="12">
    <Card>
      <CardHeader class="bg-light">Input Groups</CardHeader>

      <CardBody>
        <Row>
          <Col md="4">
            <Label>Text addon</Label>

            <InputGroup class="mb-3">
              <InputGroupAddon addonType="prepend">
                <InputGroupText>@</InputGroupText>
              </InputGroupAddon>
              <Input placeholder="Username" />
            </InputGroup>

            <InputGroup class="mb-3">
              <Input placeholder="Recipient's username" />
              <InputGroupAddon addonType="append">
                <InputGroupText>@</InputGroupText>
              </InputGroupAddon>
            </InputGroup>

            <InputGroup class="mb-3">
              <InputGroupAddon addonType="prepend">
                <InputGroupText>$</InputGroupText>
              </InputGroupAddon>
              <Input />
              <InputGroupAddon addonType="append">
                <InputGroupText>.00</InputGroupText>
              </InputGroupAddon>
            </InputGroup>
          </Col>

          <Col md="4">
            <Label>Icon addon</Label>

            <InputGroup class="mb-3">
              <InputGroupAddon addonType="prepend">
                <InputGroupText><i class="fa fa-user" /></InputGroupText>
              </InputGroupAddon>
              <Input placeholder="Username" />
            </InputGroup>

            <InputGroup class="mb-3">
              <Input placeholder="Email address" />
              <InputGroupAddon addonType="append">
                <InputGroupText><i class="fa fa-envelope" /></InputGroupText>
              </InputGroupAddon>
            </InputGroup>

            <InputGroup class="mb-3">
              <InputGroupAddon addonType="prepend">
                <InputGroupText><i class="fa fa-credit-card" /></InputGroupText>
              </InputGroupAddon>
              <Input placeholder="Card Number" />
              <InputGroupAddon addonType="append">
                <InputGroupText><i class="fa fa-hashtag" /></InputGroupText>
              </InputGroupAddon>
            </InputGroup>
          </Col>

          <Col md="4">
            <Label>Sizes</Label>

            <InputGroup class="mb-3" size="lg">
              <InputGroupAddon addonType="prepend">
                <InputGroupText>@</InputGroupText>
              </InputGroupAddon>
              <Input placeholder="Username" />
            </InputGroup>

            <InputGroup class="mb-3">
              <InputGroupAddon addonType="prepend">
                <InputGroupText>@</InputGroupText>
              </InputGroupAddon>
              <Input placeholder="Username" />
            </InputGroup>

            <InputGroup class="mb-3" size="sm">
              <InputGroupAddon addonType="prepend">
                <InputGroupText>@</InputGroupText>
              </InputGroupAddon>
              <Input placeholder="Username" />
            </InputGroup>
          </Col>
        </Row>

        <Row class="mt-4">
          <Col md="4">
            <Label for="input-group-1">Input Group with Button</Label>
            <InputGroup>
              <InputGroupAddon addonType="prepend">
                <Button color="default" style="margin-right: 1px;"
                  ><i class="fa fa-search" /> Search</Button>
              </InputGroupAddon>
              <Input placeholder="Username" />
            </InputGroup>
          </Col>

          <Col md="4">
            <Label for="input-group-2">Input Group with Button</Label>
            <InputGroup>
              <Input placeholder="Username" />
              <InputGroupAddon addonType="append">
                <Button color="default" style="margin-left: 1px;"
                  ><i class="fa fa-search" /> Search</Button>
              </InputGroupAddon>
            </InputGroup>
          </Col>

          <Col md="4">
            <Label for="input-group-3">Input Group with Dropdown</Label>
            <InputGroup>
              <InputGroupAddon addonType="prepend">
                <ButtonDropdown style="margin-right: 1px;">
                  <DropdownToggle color="default" caret>Action</DropdownToggle>
                  <DropdownMenu>
                    <DropdownItem>Action</DropdownItem>
                    <DropdownItem>Another action</DropdownItem>
                    <DropdownItem>Something else here</DropdownItem>
                    <DropdownItem divider />
                    <DropdownItem>Separated link</DropdownItem>
                  </DropdownMenu>
                </ButtonDropdown>
              </InputGroupAddon>

              <Input placeholder="Username" />
            </InputGroup>
          </Col>
        </Row>
      </CardBody>
    </Card>
  </Col>
</Row>

<style></style>
