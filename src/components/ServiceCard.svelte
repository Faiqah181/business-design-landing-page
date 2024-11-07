<script lang="ts">
  export let animationType: 1 | 2;
  export let index: number;
</script>

<li class="card" id="card1" style="--index: {index}">
  <div class="card-content" class:card-animation1={animationType === 1} class:card-animation2={animationType === 2}>
      <div class="card-header">
          <div>
              <p>1</p>
              <h1>Voice Support</h1>
          </div>
          <img alt="logo" src="crypto.svg" />
      </div>
      <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit,
          sed do eiusmod tempor incididunt ut labore et dolore
          magna aliqua.
      </p>
  </div>
</li>

<style>
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
    animation-range: entry-crossing var(--start-range) exit-crossing
      var(--end-range);
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
