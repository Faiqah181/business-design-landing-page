<script>
</script>

<div class="wave"></div>

<style>
    .wave {
        overflow: hidden;
        position: relative;
        height: 100px;
        margin-top: -4.8rem;
    }
    .wave:after {
        content: "";
        position: absolute;
        will-change: transform;
        left: 0;
        top: 0;
        bottom: 0;
        right: -300vw;
        background: var(--background-color);
        --size: 60px;
        --m: 2;
        --p: calc(var(--m) * var(--size));
        --R: calc(var(--size) * sqrt(var(--m) * var(--m) + 1));
        --mask: radial-gradient(var(--R) at left 50% top calc(var(--size) + var(--p)),#000 99%,#0000 101%)
                calc(50% - 2 * var(--size)) 0 / calc(4 * var(--size)) 100%,
                radial-gradient(var(--R) at left 50% top calc(-1 * var(--p)),#0000 99%,#000 101%)
                left 50% top var(--size) / calc(4 * var(--size)) 100% repeat-x;
        mask: var(--mask);
        -webkit-mask: var(--mask);
        animation: wave 50s linear infinite alternate;
    }
    @keyframes wave {
        100% {
            transform: translate3d(-300vw, 0, 0px);
        }
    }
</style>
