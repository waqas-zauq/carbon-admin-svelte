<script>
  import { Card, CardBody } from "sveltestrap/src";

  export let cardValue;
  export let cardText;
  export let cardIcon;
</script>

<Card class="p-4">
  <CardBody class="d-flex justify-content-between align-items-center">
    <div>
      <span class="h4 d-block font-weight-normal mb-2">{cardValue}</span>
      <span class="font-weight-light">{cardText}</span>
    </div>

    <div class="h2 text-muted">
      <i class="icon icon-{cardIcon}" />
    </div>
  </CardBody>
</Card>

<style></style>
