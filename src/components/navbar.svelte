<script>
    import LineMdCloseToMenuTransition from '~icons/line-md/close-to-menu-transition';
    import LineMdMenuToCloseTransition from '~icons/line-md/menu-to-close-transition';
    import GameIconsBoomerangSun from '~icons/game-icons/boomerang-sun';
    let nav = false;
</script>

<div class="navbar">
    <div class="logo">
        <GameIconsBoomerangSun width='2rem' height='2rem' />
        <span>Creative Labs</span>
    </div>
    <button class="menu-button" on:click={() => nav = !nav}>
        {#if nav}
            <LineMdMenuToCloseTransition />
        {:else}
            <LineMdCloseToMenuTransition />
        {/if}
    </button>
</div>

<style>

    .navbar{
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 1rem;
        height: var(--nav-height);
        color: white;
        position: sticky;
        z-index: 50;
        top: 0;
    }

    .menu-button {
        font-size: 1.2rem;
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 3rem;
        width: 3rem;
        padding: 0.5rem;
        border-radius: 50rem;
        border: 0;
        background-color: var(--background-color);
        transition: all 0.3s;
    }
    .menu-button:hover {
        scale: 1.15;
    }

    .logo {
        display: flex;
        gap: 0.75rem;
        align-items: center;
    }

    .logo span {
        font-size: 1.5rem;
    }
</style>
