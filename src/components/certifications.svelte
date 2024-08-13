<script>
    import IsoLogo from "../assets/ISO-log.png";
</script>

<div class="element">
    <div class="heading">
        <span>Certifications</span>
    </div>
    <div class="main">
        <ul class="cards">
            <li id="card1" class="card">
                <div class="card-content">
                    <img alt="iso-logo" src={IsoLogo} />
                    <span>ISO - 14001</span>
                </div>
            </li>
            <li id="card2" class="card">
                <div class="card-content">
                    <img alt="iso-logo" src={IsoLogo} />
                    <span>ISO - 14002</span>
                </div>
            </li>
            <li id="card3" class="card">
                <div class="card-content">
                    <img alt="iso-logo" src={IsoLogo} />
                    <span>ISO - 14003</span>
                </div>
            </li>
            <li id="card4" class="card">
                <div class="card-content">
                    <img alt="iso-logo" src={IsoLogo} />
                    <span>ISO - 14004</span>
                </div>
            </li>
            <li id="card5" class="card">
                <div class="card-content">
                    <img alt="iso-logo" src={IsoLogo} />
                    <span>ISO - 14005</span>
                </div>
            </li>
        </ul>
    </div>
</div>

<style>
    li {
        list-style: none;
    }

    .element {
        padding-top: 2rem;
        display: flex;
        flex-direction: column;
        view-timeline-name: --cert-scrolling-body;
    }

    .heading {
        align-self: center;
        padding-top: 1rem;
        font-size: 3rem;
        position: sticky;
        top: 0%;
        z-index: -100;
    }

    .main {
        height: 900vh;
        width: 100vw;
        overflow: visible;
        z-index: 100;
    }

    .cards {
        display: flex;
        flex-direction: row;
        overflow: clip;
        height: 100vh;
        width: 900vw;
        position: sticky;
        top: 0%;
    }

    #card1 {
        --index: 1;
    }
    #card1 div {
        background-color: rgb(70, 16, 208);
    }

    #card2 {
        --index: 2;
    }
    #card2 div {
        background-color: rgb(255, 0, 85);
    }

    #card3 {
        --index: 3;
    }
    #card3 div {
        background-color: rgb(0, 0, 0);
    }

    #card4 {
        --index: 4;
    }
    #card4 div {
        background-color: rgb(70, 16, 208);
    }

    #card5 {
        --index: 5;
    }
    #card5 div {
        background-color: rgb(255, 0, 85);
    }

    .card {
        margin-top: 2rem;
        transform: translateX(calc(100vw * var(--index)));
    }

    .card-content {
        display: flex;
        flex-direction: column;
        gap: 2rem;
        justify-content: center;
        align-items: center;
        border: 1px solid rgb(172, 1, 58);
        height: 18rem;
        width: 12rem;
        color: white;
        animation: card-flying-in linear both;
        animation-timeline: --cert-scrolling-body;
        animation-range: entry-crossing exit-crossing;
    }

    .card-content img {
        width: 70%;
        height: 60%;
    }

    @keyframes card-flying-in {
        0% {
            transform: translateY(-40vh);
        }
        80% {
            transform: translateX(calc(-90vw * var(--index))) translateY(30vh)
                rotateZ(20deg);
        }
        100% {
            transform: translateX(calc(-95vw * var(--index))) translateY(-30vh)
                rotateZ(-20deg);
        }
    }
</style>
