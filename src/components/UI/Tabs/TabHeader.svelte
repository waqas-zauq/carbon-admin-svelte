<script>
  export let id = "svelte";
</script>

<ul class="nav nav-tabs" {id} role="tablist">
  <slot />
</ul>
