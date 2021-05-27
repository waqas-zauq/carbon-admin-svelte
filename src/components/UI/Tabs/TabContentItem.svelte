<script>
  export let id;
</script>

<div class="tab-pane fade" {id} role="tabpanel" aria-labelledby={`${id}-tab`}>
  <slot />
</div>
