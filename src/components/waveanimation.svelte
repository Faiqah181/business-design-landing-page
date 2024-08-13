<script>
</script>

<div class="wave" style="margin-top: -3rem;"></div>

<style>
    .wave {
        overflow: hidden;
        position: relative;
        height: 100px;
    }
    .wave:after {
        content: "";
        position: absolute;
        will-change: transform;
        left: 0;
        top: 0;
        bottom: 0;
        right: -300vw;
        background: rgb(255, 255, 255);
        --mask: radial-gradient(75.15px at 50% 101.5px, #000 99%, #0000 101%)
                calc(50% - 70px) 0/140px 100%,
            radial-gradient(75.15px at 50% -66.5px, #0000 99%, #000 101%) 50%
                35px/140px 100% repeat-x;
        -webkit-mask: var(--mask);
        mask: var(--mask);
        animation: wave 50s linear infinite alternate;
    }
    @keyframes wave {
        100% {
            transform: translate3d(-300vw, 0, 0px);
        }
    }
</style>
