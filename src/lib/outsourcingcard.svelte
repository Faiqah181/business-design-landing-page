<script>
    export let logo;
    export let cardColor;
    export let text;
    export let rotate;
    export let animationDelay;
</script>

<div class="card" style="--cardColor:{cardColor}; --rotate:{rotate}; --animationDelay:{animationDelay};">
    <img src={logo} alt="icon" />
    <span>{text}</span>
</div>

<style>
    .card {
        background-color: var(--cardColor);
        display: flex;
        opacity: 0%;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 1.5rem;
        height: 24rem;
        width: 18rem;
        color: white;
        padding: 0.5rem;
        border: 1px solid var(--cardColor);
        border-radius: 5%;
        animation-name: card;
        animation-duration: 5s;
        animation-delay: var(--animationDelay);
        animation-iteration-count: infinite;
    }

    .card span {
        text-align: center;
        font-family: monospace;
        font-size: 2rem;
        line-height: 2.25rem;
    }

    .card img{
        width: 20%;
        height: 20%;
    }

    @keyframes card{
        0%{
            bottom: 0px;
            opacity: 80%;
            display: flex;
            transform: translate3d(0, 500px, 0) rotate(var(--rotate));
        }

        100% {
            top: 200%;
            opacity: 100%;
            transform: translate3d(0, -700px, 0) rotate(10deg);
        }
    }

</style>
