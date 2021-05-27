<script>
  export let id = "svelte";
</script>

<div class="tab-content" id={`${id}Content`}>
  <slot />
</div>

<style>
  .tab-content {
    padding: 20px 0;
  }
</style>
