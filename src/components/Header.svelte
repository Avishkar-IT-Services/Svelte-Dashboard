<script>
    import SearchBar from "./SearchBar.svelte";
    import {
        Collapse,
        Navbar,
        NavbarToggler,
        NavbarBrand,
        Nav,
        NavItem,
        NavLink,
        Dropdown,
        DropdownToggle,
        DropdownMenu,
        DropdownItem,
    } from "sveltestrap";

    let isOpen = false;

    function handleUpdate(event) {
        isOpen = event.detail.isOpen;
    }
</script>

<Navbar color="dark" light expand="md" class="nav__bar">
    <NavbarBrand class="nav__bar">Svelte-Dashboard</NavbarBrand>
    <NavbarToggler on:click={() => (isOpen = !isOpen)} />
    <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
        <Nav class="ms-auto" navbar>
            <NavItem>
                <SearchBar />
            </NavItem>
            <Dropdown nav inNavbar>
                <DropdownToggle nav caret class="text-white">
                  Profile
                </DropdownToggle>
                <DropdownMenu end>
                    <DropdownItem>Setting</DropdownItem>
                    <DropdownItem>Activity Log</DropdownItem>
                    <DropdownItem divider />
                    <DropdownItem>Logout</DropdownItem>
                </DropdownMenu>
            </Dropdown>
        </Nav>
    </Collapse>
</Navbar>

<style>
    :global(.nav__bar) {
        color: white !important;
    }
</style>
