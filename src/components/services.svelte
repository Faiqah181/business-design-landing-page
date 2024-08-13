<script>
</script>

<div class="element">
    <div class="heading">Our Services</div>
    <div class="main">
        <ul class="cards">
            <li class="card" id="card1">
                <div class="card-content card-animation1">
                    <div class="card-header">
                        <div>
                            <p>1</p>
                            <h1>Voice Support</h1>
                        </div>
                        <img alt="logo" />
                    </div>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua.
                    </p>
                </div>
            </li>
            <li class="card" id="card2">
                <div class="card-content card-animation2">
                    <div class="card-header">
                        <div>
                            <p>2</p>
                            <h1>Live Chat</h1>
                        </div>
                        <img alt="logo" />
                    </div>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua.
                    </p>
                </div>
            </li>
            <li class="card" id="card3">
                <div class="card-content card-animation1">
                    <div class="card-header">
                        <div>
                            <p>3</p>
                            <h1>Email Support</h1>
                        </div>
                        <img alt="logo" />
                    </div>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua.
                    </p>
                </div>
            </li>
            <li class="card" id="card4">
                <div class="card-content card-animation2">
                    <div class="card-header">
                        <div>
                            <p>4</p>
                            <h1>Technical Support</h1>
                        </div>
                        <img alt="logo" />
                    </div>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua.
                    </p>
                </div>
            </li>
            <li class="card" id="card5">
                <div class="card-content card-animation1">
                    <div class="card-header">
                        <div>
                            <p>5</p>
                            <h1>Lead Generatioon</h1>
                        </div>
                        <img alt="logo" />
                    </div>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua.
                    </p>
                </div>
            </li>
        </ul>
    </div>
</div>

<style>
    #card1 {
        --index: 1;
    }
    #card2 {
        --index: 2;
    }
    #card3 {
        --index: 3;
    }
    #card4 {
        --index: 4;
    }
    #card5 {
        --index: 5;
    }

    .element {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        height: 100rem;
        view-timeline-name: --service-scrolling-body;
        padding-left: 4rem;
        gap: 20rem;
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

    .card {
        position: sticky;
        top: 5%;
        padding-top: calc(var(--index) * 1em);
    }

    .card-header {
        display: flex;
        justify-content: space-between;
    }

    .card-header h1 {
        margin: 0;
        font-size: 2.75rem;
    }

    .card-content {
        border: 2px solid black;
        background-color: white;
        color: black;
        display: flex;
        flex-direction: column;
        gap: 2rem;
        padding: 1rem;
        width: 70%;
        overflow: hidden;
    }

    .card-animation1 {
        --index0: calc(var(--index) - 1);
        --start-range: calc(calc(var(--index0) * 2) / 100 * 100%);
        --end-range: calc(calc(var(--index) * 2) / 100 * 100%);
        animation: card-rotation1 linear both;
        animation-timeline: --service-scrolling-body;
        animation-range: entry-crossing var(--start-range) exit-crossing var(--end-range);
    }

    @keyframes card-rotation1 {
        45% {
            background-color: white;
            color: black;
        }
        46% {
            background-color: blue;
            transform: rotateZ(5deg);
        }
        80% {
            background-color: blue;
            color: white;
            transform: rotateZ(5deg);
        }
        100% {
            background-color: white;
            color: black;
            transform: rotateZ(5deg);
        }
    }

    .card-animation2 {
        --index0: calc(var(--index) - 1);
        --start-range: calc(calc(var(--index0) * 12) / 100 * 100%);
        --end-range: calc(calc(var(--index) * 12) / 100 * 100%);
        animation: card-rotation2 linear both;
        animation-timeline: --service-scrolling-body;
        animation-range: contain var(--start-range) exit-crossing var(--end-range);
    }

    @keyframes card-rotation2 {
        35% {
            background-color: white;
            color: black;
        }
        36% {
            background-color: rgb(208, 100, 132);
            transform: rotateZ(-5deg);
        }
        90% {
            background-color: rgb(208, 100, 132);
            color: white;
            transform: rotateZ(-5deg);
        }
        100% {
            background-color: white;
            color: black;
            transform: rotateZ(-5deg);
        }
    }
</style>
