<script>
  import { Card, CardBody, Progress } from "sveltestrap/src";

  export let cardValue;
  export let cardText;
  export let cardProgressBarValue;
  export let cardProgressBarColor;
</script>

<Card>
  <CardBody class="p-5">
    <div class="text-center">
      <span class="h4 d-block font-weight-normal mb-2">{cardValue}</span>
      <span class="font-weight-light">{cardText}</span>
    </div>

    <div class="mt-4">
      <Progress value={cardProgressBarValue} color={cardProgressBarColor} />
    </div>
  </CardBody>
</Card>

<style></style>
