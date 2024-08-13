<script>
    import Outsourcingcard from "../lib/outsourcingcard.svelte";
    import Logo from "../assets/svelte.svg"
</script>

<div class="card">
    <span class="heading"> OUTSOURCING? </span>
    <span class="subheading"> LET'S ADDRESS YOUR WORRIES </span>
    <div class="subcards">
        <Outsourcingcard text="Cultural and Language Barriers" cardColor="#0F2084" rotate="15deg" logo={Logo} animationDelay='0s'/>
        <Outsourcingcard text="Technical Proficiency in SaaS Support" cardColor="#AD2084" rotate="-15deg" logo={Logo} animationDelay='3s'/>
        <Outsourcingcard text="Seasonal Workload Scalibility" cardColor="#4A0084" rotate="25deg" logo={Logo} animationDelay='6s'/>
    </div>
</div>

<style>
    .card {
        width: 100%;
        height: 100vh;
        background-color: rgb(255, 255, 255);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .heading {
        font-size: 4.5rem;
        font-weight: 100;
        font-family: system-ui;
        z-index: 100;
    }

    .subheading {
        font-size: 4.5rem;
        font-family: system-ui;
        font-weight: bolder;
        line-height: 1;
        z-index: 100;
    }

    .subcards{
        display: flex;
        flex-direction: row;
        gap: 12rem;
    }

</style>
