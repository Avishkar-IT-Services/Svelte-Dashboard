<script>
    import { navigate } from "svelte-routing";
    const handleMenu = (path) => {
        navigate(path);
    };
    const navItems = [
        { title: "Dashboard", link: "/" },
        { title: "Setting", link: "/setting" },
        { title: "Contact", link: "/contact" },
    ];
</script>

<div class="dash__parent">
    <div class="dash__side--bar">
        {#each navItems as { title, link }, i}
            <!-- svelte-ignore a11y-click-events-have-key-events -->
            <div on:click={() => handleMenu(link)}>{title}</div>
        {/each}
    </div>
</div>

<style>
    .dash__parent {
        width: 100vw;
        display: flex;
    }
    .dash__side--bar {
        padding: 1%;
        width: 15vw;
        background-color: #212529;
        height: 93vh;
        color: white;
    }

    .dash__side--bar > div {
        margin: 7%;
        font-size: 19px;
        cursor: pointer;
    }
</style>
