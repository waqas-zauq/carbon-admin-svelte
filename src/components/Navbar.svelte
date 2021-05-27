<script>
  import { createEventDispatcher } from "svelte";
  import {
    Navbar,
    NavbarBrand,
    Nav,
    NavItem,
    NavLink,
    Dropdown,
    DropdownToggle,
    DropdownMenu,
    DropdownItem
  } from "sveltestrap/src";

  const dispatch = createEventDispatcher();
</script>

<Navbar expand="md" class="page-header">
  <!-- svelte-ignore a11y-invalid-attribute -->
  <a
    href="javascript:void(0);"
    class="btn btn-link sidebar-mobile-toggle d-md-none mr-auto"
    on:click={() => {
      dispatch("toggleSidebarMobile");
    }}>
    <i class="fa fa-bars" />
  </a>

  <NavbarBrand href="/">
    <img src="theme/imgs/logo.png" alt="logo" />
  </NavbarBrand>

  <!-- svelte-ignore a11y-invalid-attribute -->
  <a
    href="javascript:void(0);"
    class="btn btn-link sidebar-toggle d-md-down-none"
    on:click={() => {
      dispatch("toggleSidebar");
    }}>
    <i class="fa fa-bars" />
  </a>

  <Nav class="ml-auto" navbar>
    <NavItem class="d-md-down-none">
      <NavLink href="#">
        <i class="fa fa-bell" />
        <span class="badge badge-pill badge-danger">5</span>
      </NavLink>
    </NavItem>
    <NavItem class="d-md-down-none">
      <NavLink href="#">
        <i class="fa fa-envelope-open" />
        <span class="badge badge-pill badge-danger">5</span>
      </NavLink>
    </NavItem>
    <Dropdown nav inNavbar>
      <DropdownToggle nav caret>
        <img
          src="theme/imgs/avatar-1.png"
          class="avatar avatar-sm"
          alt="logo" />
        <span class="small ml-1 d-md-down-none">John Smith</span>
      </DropdownToggle>
      <DropdownMenu right>
        <div class="dropdown-header">Account</div>
        <DropdownItem><i class="fa fa-user" /> Profile</DropdownItem>
        <DropdownItem><i class="fa fa-envelope" /> Messages</DropdownItem>
        <div class="dropdown-header">Settings</div>
        <DropdownItem><i class="fa fa-bell" /> Notifications</DropdownItem>
        <DropdownItem><i class="fa fa-wrench" /> Settings</DropdownItem>
        <DropdownItem><i class="fa fa-lock" /> Logout</DropdownItem>
      </DropdownMenu>
    </Dropdown>
  </Nav>
</Navbar>
