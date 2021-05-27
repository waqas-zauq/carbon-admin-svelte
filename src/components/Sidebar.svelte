<script>
  import { Nav } from "sveltestrap/src";
  import { stores } from "@sapper/app";

  import SidebarItem from "./SidebarItem.svelte";

  const { page } = stores();

  $: navigation = [
    {
      type: "title",
      name: "Navigation"
    },
    {
      type: "item",
      name: "Dashboard",
      icon: "speedometer",
      address: "/",
      isParent: false,
      isActive: $page.path === "/"
    },
    {
      type: "item",
      name: "Layouts",
      icon: "target",
      address: "javascript:void(0);",
      isOpen: $page.path.startsWith("/layouts"),
      isParent: true,
      children: [
        {
          type: "item",
          name: "Normal",
          icon: "target",
          address: "layouts/layouts-normal",
          isParent: false,
          isActive: $page.path === "/layouts/layouts-normal"
        },
        {
          type: "item",
          name: "Fixed Sidebar",
          icon: "target",
          address: "layouts/layouts-fixed-sidebar",
          isParent: false,
          isActive: $page.path === "/layouts/layouts-fixed-sidebar"
        },
        {
          type: "item",
          name: "Fixed Header",
          icon: "target",
          address: "layouts/layouts-fixed-header",
          isParent: false,
          isActive: $page.path === "/layouts/layouts-fixed-header"
        },
        {
          type: "item",
          name: "Hidden Sidebar",
          icon: "target",
          address: "layouts/layouts-hidden-sidebar",
          isParent: false,
          isActive: $page.path === "/layouts/layouts-hidden-sidebar"
        }
      ]
    },
    {
      type: "item",
      name: "UI Kits",
      icon: "energy",
      address: "javascript:void(0);",
      isOpen: $page.path.startsWith("/ui-kits"),
      isParent: true,
      children: [
        {
          type: "item",
          name: "Alerts",
          icon: "energy",
          address: "ui-kits/alerts",
          isParent: false,
          isActive: $page.path === "/ui-kits/alerts"
        },
        {
          type: "item",
          name: "Buttons",
          icon: "energy",
          address: "ui-kits/buttons",
          isParent: false,
          isActive: $page.path === "/ui-kits/buttons"
        },
        {
          type: "item",
          name: "Cards",
          icon: "energy",
          address: "ui-kits/cards",
          isParent: false,
          isActive: $page.path === "/ui-kits/cards"
        },
        {
          type: "item",
          name: "Modals",
          icon: "energy",
          address: "ui-kits/modals",
          isParent: false,
          isActive: $page.path === "/ui-kits/modals"
        },
        {
          type: "item",
          name: "Tabs",
          icon: "energy",
          address: "ui-kits/tabs",
          isParent: false,
          isActive: $page.path === "/ui-kits/tabs"
        },
        {
          type: "item",
          name: "Progress Bars",
          icon: "energy",
          address: "ui-kits/progress-bars",
          isParent: false,
          isActive: $page.path === "/ui-kits/progress-bars"
        },
        {
          type: "item",
          name: "Widgets",
          icon: "energy",
          address: "ui-kits/widgets",
          isParent: false,
          isActive: $page.path === "/ui-kits/widgets"
        }
      ]
    },
    {
      type: "item",
      name: "Charts",
      icon: "graph",
      address: "javascript:void(0);",
      isOpen: $page.path.startsWith("/charts"),
      isParent: true,
      children: [
        {
          type: "item",
          name: "Chart.js",
          icon: "energy",
          address: "charts/chartjs",
          isParent: false,
          isActive: $page.path === "/charts/chartjs"
        }
      ]
    },
    {
      type: "item",
      name: "Forms",
      icon: "puzzle",
      address: "forms",
      isParent: false,
      isActive: $page.path === "/forms"
    },
    {
      type: "item",
      name: "Tables",
      icon: "grid",
      address: "tables",
      isParent: false,
      isActive: $page.path === "/tables"
    },
    {
      type: "title",
      name: "More"
    },
    {
      type: "item",
      name: "Pages",
      icon: "umbrella",
      address: "javascript:void(0);",
      isOpen: $page.path.startsWith("/pages"),
      isParent: true,
      children: [
        {
          type: "item",
          name: "Blank Page",
          icon: "umbrella",
          address: "pages/blank",
          isParent: false,
          isActive: $page.path === "/pages/blank"
        },
        {
          type: "item",
          name: "Login",
          icon: "umbrella",
          address: "pages/login",
          isParent: false,
          isActive: $page.path === "/pages/login"
        },
        {
          type: "item",
          name: "Register",
          icon: "umbrella",
          address: "pages/register",
          isParent: false,
          isActive: $page.path === "/pages/register"
        },
        {
          type: "item",
          name: "Invoice",
          icon: "umbrella",
          address: "pages/invoice",
          isParent: false,
          isActive: $page.path === "/pages/invoice"
        },
        {
          type: "item",
          name: "404",
          icon: "umbrella",
          address: "pages/404",
          isParent: false,
          isActive: $page.path === "/pages/404"
        },
        {
          type: "item",
          name: "500",
          icon: "umbrella",
          address: "pages/500",
          isParent: false,
          isActive: $page.path === "/pages/500"
        },
        {
          type: "item",
          name: "Settings",
          icon: "umbrella",
          address: "pages/settings",
          isParent: false,
          isActive: $page.path === "/pages/settings"
        }
      ]
    }
  ];
</script>

<div class="sidebar">
  <nav class="sidebar-nav">
    <Nav>
      {#each navigation as sidebarItem (sidebarItem.name)}
        <SidebarItem {sidebarItem} />
      {/each}
    </Nav>
  </nav>
</div>
