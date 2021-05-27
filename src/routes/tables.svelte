<script>
  import { Row, Col, Card, CardHeader, CardBody, Table } from "sveltestrap/src";
  import data from "./data.example.js";
  import { Datatable, rows } from "svelte-simple-datatables";

  const settings = { columnFilter: true };
</script>

<svelte:head>
  <title>Tables</title>
</svelte:head>

<Row>
  <Col md="6">
    <Card>
      <CardHeader class="bg-light">Normal Table</CardHeader>

      <CardBody>
        <Table responsive>
          <thead>
            <tr>
              <th>ID</th>
              <th>Name</th>
              <th>Sales</th>
              <th>Price</th>
              <th>Discount</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>1</td>
              <td class="text-nowrap">Samsung Galaxy S8</td>
              <td>31,589</td>
              <td>$800</td>
              <td>5%</td>
            </tr>
            <tr>
              <td>2</td>
              <td class="text-nowrap">Google Pixel XL</td>
              <td>99,542</td>
              <td>$750</td>
              <td>3%</td>
            </tr>
            <tr>
              <td>3</td>
              <td class="text-nowrap">iPhone X</td>
              <td>62,220</td>
              <td>$1,200</td>
              <td>0%</td>
            </tr>
            <tr>
              <td>4</td>
              <td class="text-nowrap">OnePlus 5T</td>
              <td>50,000</td>
              <td>$650</td>
              <td>5%</td>
            </tr>
            <tr>
              <td>5</td>
              <td class="text-nowrap">Google Nexus 6</td>
              <td>400</td>
              <td>$400</td>
              <td>7%</td>
            </tr>
          </tbody>
        </Table>
      </CardBody>
    </Card>
  </Col>

  <Col md="6">
    <Card>
      <CardHeader class="bg-light">Striped Rows</CardHeader>

      <CardBody>
        <Table striped responsive>
          <thead>
            <tr>
              <th>ID</th>
              <th>Name</th>
              <th>Sales</th>
              <th>Price</th>
              <th>Discount</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>1</td>
              <td class="text-nowrap">Samsung Galaxy S8</td>
              <td>31,589</td>
              <td>$800</td>
              <td>5%</td>
            </tr>
            <tr>
              <td>2</td>
              <td class="text-nowrap">Google Pixel XL</td>
              <td>99,542</td>
              <td>$750</td>
              <td>3%</td>
            </tr>
            <tr>
              <td>3</td>
              <td class="text-nowrap">iPhone X</td>
              <td>62,220</td>
              <td>$1,200</td>
              <td>0%</td>
            </tr>
            <tr>
              <td>4</td>
              <td class="text-nowrap">OnePlus 5T</td>
              <td>50,000</td>
              <td>$650</td>
              <td>5%</td>
            </tr>
            <tr>
              <td>5</td>
              <td class="text-nowrap">Google Nexus 6</td>
              <td>400</td>
              <td>$400</td>
              <td>7%</td>
            </tr>
          </tbody>
        </Table>
      </CardBody>
    </Card>
  </Col>
</Row>

<Row>
  <Col md="6">
    <Card>
      <CardHeader class="bg-light">Bordered Table</CardHeader>

      <CardBody>
        <Table bordered responsive>
          <thead>
            <tr>
              <th>ID</th>
              <th>Name</th>
              <th>Sales</th>
              <th>Price</th>
              <th>Discount</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>1</td>
              <td class="text-nowrap">Samsung Galaxy S8</td>
              <td>31,589</td>
              <td>$800</td>
              <td>5%</td>
            </tr>
            <tr>
              <td>2</td>
              <td class="text-nowrap">Google Pixel XL</td>
              <td>99,542</td>
              <td>$750</td>
              <td>3%</td>
            </tr>
            <tr>
              <td>3</td>
              <td class="text-nowrap">iPhone X</td>
              <td>62,220</td>
              <td>$1,200</td>
              <td>0%</td>
            </tr>
            <tr>
              <td>4</td>
              <td class="text-nowrap">OnePlus 5T</td>
              <td>50,000</td>
              <td>$650</td>
              <td>5%</td>
            </tr>
            <tr>
              <td>5</td>
              <td class="text-nowrap">Google Nexus 6</td>
              <td>400</td>
              <td>$400</td>
              <td>7%</td>
            </tr>
          </tbody>
        </Table>
      </CardBody>
    </Card>
  </Col>

  <Col md="6">
    <Card>
      <CardHeader class="bg-light">Hoverable Table</CardHeader>

      <CardBody>
        <Table hover responsive>
          <thead>
            <tr>
              <th>ID</th>
              <th>Name</th>
              <th>Sales</th>
              <th>Price</th>
              <th>Discount</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>1</td>
              <td class="text-nowrap">Samsung Galaxy S8</td>
              <td>31,589</td>
              <td>$800</td>
              <td>5%</td>
            </tr>
            <tr>
              <td>2</td>
              <td class="text-nowrap">Google Pixel XL</td>
              <td>99,542</td>
              <td>$750</td>
              <td>3%</td>
            </tr>
            <tr>
              <td>3</td>
              <td class="text-nowrap">iPhone X</td>
              <td>62,220</td>
              <td>$1,200</td>
              <td>0%</td>
            </tr>
            <tr>
              <td>4</td>
              <td class="text-nowrap">OnePlus 5T</td>
              <td>50,000</td>
              <td>$650</td>
              <td>5%</td>
            </tr>
            <tr>
              <td>5</td>
              <td class="text-nowrap">Google Nexus 6</td>
              <td>400</td>
              <td>$400</td>
              <td>7%</td>
            </tr>
          </tbody>
        </Table>
      </CardBody>
    </Card>
  </Col>
</Row>

<Row>
  <Col md="12">
    <Card style="height: 500px; overflow:auto;">
      <CardHeader class="bg-light">Datatable</CardHeader>

      <CardBody>
        <Datatable {settings} {data}>
          <thead>
            <th data-key="first_name">First Name</th>
            <th data-key="last_name">Last Name</th>
            <th data-key="email">Email</th>
          </thead>
          <tbody>
            {#each $rows as row}
              <tr>
                <td>{row.first_name}</td>
                <td>{row.last_name}</td>
                <td>{row.email}</td>
              </tr>
            {/each}
          </tbody>
        </Datatable>
      </CardBody>
    </Card>
  </Col>
</Row>

<style></style>
