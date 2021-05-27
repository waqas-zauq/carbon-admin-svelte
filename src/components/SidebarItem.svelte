<script>
  export let sidebarItem;
</script>

{#if sidebarItem.type === "title"}
  <li class="nav-title">{sidebarItem.name}</li>
{:else if sidebarItem.isParent}
  <li class="nav-item nav-dropdown" class:open={sidebarItem.isOpen}>
    <a
      href={sidebarItem.address}
      class="nav-link nav-dropdown-toggle"
      on:click={() => {
        sidebarItem.isOpen = !sidebarItem.isOpen;
      }}>
      <i class="icon icon-{sidebarItem.icon}" />
      {sidebarItem.name}
      <i class="fa fa-caret-left" />
    </a>

    <ul class="nav-dropdown-items">
      {#each sidebarItem.children as child (child.name)}
        <svelte:self sidebarItem={child} on:checkActive />
      {/each}
    </ul>
  </li>
{:else}
  <li class="nav-item">
    <a
      href={sidebarItem.address}
      class="nav-link"
      class:active={sidebarItem.isActive}>
      <i class="icon icon-{sidebarItem.icon}" />
      {sidebarItem.name}
    </a>
  </li>
{/if}

<style>
</style>
