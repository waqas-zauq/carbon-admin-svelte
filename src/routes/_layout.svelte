<script>
  import { stores } from "@sapper/app";
  import { Container } from "sveltestrap/src";

  import Navbar from "../components/Navbar.svelte";
  import Sidebar from "../components/Sidebar.svelte";

  export let segment;

  const { page } = stores();

  let sidebarHidden = false;
  let sidebarHiddenMobile = true;

  function toggleSidebar() {
    sidebarHidden = !sidebarHidden;
    sidebarHidden
      ? document.body.classList.add("sidebar-hidden")
      : document.body.classList.remove("sidebar-hidden");
  }

  function toggleSidebarMobile() {
    sidebarHiddenMobile = !sidebarHiddenMobile;
    sidebarHiddenMobile
      ? document.body.classList.remove("sidebar-mobile-show")
      : document.body.classList.add("sidebar-mobile-show");
  }
</script>

<svelte:head>
  <title>Carbon - Admin Template</title>
</svelte:head>

{#if segment !== "pages" || $page.path === "/pages/blank" || $page.path === "/pages/invoice" || $page.path === "/pages/settings"}
  <div class="page-wrapper">
    <Navbar
      on:toggleSidebar={toggleSidebar}
      on:toggleSidebarMobile={toggleSidebarMobile} />

    <div class="main-container">
      <Sidebar />

      <div class="content">
        {#if $page.path === "/pages/invoice"}
          <Container>
            <main>
              <slot />
            </main>
          </Container>
        {:else}
          <Container fluid>
            <main>
              <slot />
            </main>
          </Container>
        {/if}
      </div>
    </div>
  </div>
{:else}
  <div class="page-wrapper flex-row align-items-center">
    <Container>
      <main>
        <slot />
      </main>
    </Container>
  </div>
{/if}

<style>
</style>
