<script>

  let innerWidth = 0
  let innerHeight = 0

  $: screenRatio = innerWidth / innerHeight;
</script>

<svelte:window bind:innerWidth bind:innerHeight />

<div class="header">
  <video
    src="home-anim.mp4"
    class="intro-video"
    class:vh100={screenRatio <= (16/9)}
    class:vw100={screenRatio > (16/9)}
    autoplay muted loop defaultplaybackrate=2
  />
  <div class="title">
    <h1>
      MAKING YOUR WEB3 IMAGINATIONS
      A REALITY.</h1>
    <span>Now introducing the world's most powerful AI tool "Lallu.ai"</span>
  </div>
</div>

<style>
  .intro-video {
    position: relative;
    top: calc(var(--nav-height) * -1);
    z-index: -5;
    /* mask-image: linear-gradient(
      to bottom,
      rgba(0, 0, 0, 1) 80%,
      rgb(0 0 0 / 0%)
    ); */
  }
  .intro-video.vh100 {
    height: var(--video-max-height);
  }
  .intro-video.vw100 {
    width: 100dvw;
  }

  .header {
    height: calc(100vh - var(--nav-height));
    position: relative;
  }

  .title {
    position: absolute;
    bottom: 5rem;
    color: white;
    margin-left: 2rem;
  }

  .title h1 {
    margin: 0;
    font-size: 3.5rem;
    font-weight: 600;
    white-space: pre-line;
  }

  .title span {
    font-size: 2rem;
    font-style: italic;
  }
</style>
