<script>
    import Logo from "../assets/svelte.svg";
</script>

<div class="navbar">
    <div class="logo">
        <img src={Logo} alt="Logo" />
    </div>
    <div class="buttons">
        <span>About</span>
        <span>Menu</span>
        <span>Contact Us</span>
    </div>
</div>

<style>

    .navbar{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        background-color: (var(--primary-color));
        padding: 1rem;
    }

    .buttons {
        display: flex;
        gap: 2rem;
    }
</style>
