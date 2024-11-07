<script>
    import ServiceCard from "./ServiceCard.svelte";

</script>

<div class="element">
    <div class="heading">Our Services</div>
    <div class="main">
        <ul class="cards">
            <ServiceCard index={1} animationType={1} />
            <ServiceCard index={2} animationType={2} />
            <ServiceCard index={3} animationType={1} />
            <ServiceCard index={4} animationType={2} />
            <ServiceCard index={5} animationType={1} />
        </ul>
    </div>
</div>

<style>
    .element {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        /* height: 100rem; */
        view-timeline-name: --service-scrolling-body;
        padding-left: 4rem;
        gap: 20rem;
        background-color: var(--background-color);
    }

    .heading {
        font-size: 4rem;
        padding: 2rem 1rem;
        position: sticky;
        top: 10%;
        height: 80vh;
        animation-timeline: --service-scrolling-body;
    }

    p {
        margin: 0;
        padding: 0;
    }

    .main {
        overflow: visible;
        --card-count: 5;
        height: 90rem;
    }

    .cards {
        list-style: none;
        padding-bottom: calc(var(--card-count) * 2em);
    }

    
</style>
