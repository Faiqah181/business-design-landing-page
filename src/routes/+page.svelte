<script>
    import Certifications from "../components/certifications.svelte";
    import Description from "../components/description.svelte";
    import Navbar from "../components/navbar.svelte";
    import Outsourcing from "../components/outsourcing.svelte";
    import Services from "../components/services.svelte";
    import Waveanimation from "../components/waveanimation.svelte";
</script>

<div class="page">
    <div class="navbar">
        <Navbar />
    </div>
    <Description />
    <Waveanimation />
    <!--<Outsourcing />-->
    <Services />
    <Description />
    <Certifications/>
    <Description />
    <Description />
    <Description />

</div>

<style>
    .page {
        overflow: clip;
    }

    .navbar {
        position: static;
        top: 0%;
    }

    @keyframes rotateAnimation {
        0% {
            transform: rotate(0deg);
        }
        50% {
            transform: rotate(90deg);
        }
        100%{
            transform: rotate(130deg);
        }
    }
</style>
