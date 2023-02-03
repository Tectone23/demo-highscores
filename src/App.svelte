<script lang="ts">
  const scores: {
    id: string;
    score: number;
  }[] = [
    {
      id: "",
      score: 0,
    },
  ];
</script>

<main>
  <h1 class="container">
    <p id="heading" class="glitch">
      <span aria-hidden="true">codepen</span>
      codepen
      <span aria-hidden="true">codepen</span>
    </p>
  </h1>
  <div class="container scores no-scrollbar">
    <div class="top first">
      <h2 class="rank">1st</h2>
      <h2 class="name">thepiguy</h2>
    </div>
    <div class="top second">
      <h2 class="rank">2nd</h2>
      <h2 class="name">thepiguy</h2>
    </div>
    <div class="top third">
      <h2 class="rank">3rd</h2>
      <h2 class="name">thepiguy</h2>
    </div>
  </div>
</main>

<style>
  .container.scores {
    height: 100%;
    width: 100%;
    overflow-y: scroll;
    font: Inter;
  }

  .top {
    display: flex;
    flex-direction: row;
    gap: 8px;
  }

  .rank,
  .name {
    font-family: "Audiowide";
    text-transform: uppercase;
  }

  .top:nth-child(1) {
    font-size: 1.7rem;
  }
  .top:nth-child(2) {
    font-size: 1.3rem;
  }
  .top:nth-child(3) {
    font-size: 1.1rem;
  }


  h1.container {
    align-items: center;
  }


  .glitch {
    font-size: 2rem;
    position: absolute;
    font-weight: bold;
    text-transform: uppercase;
    position: relative;
    text-shadow: 0.05em 0 0 #00fffc, -0.03em -0.04em 0 #fc00ff,
      0.025em 0.04em 0 #fffc00;
    animation: glitch 725ms infinite;
  }

  .glitch span {
    position: absolute;
    top: 0;
    left: 0;
  }

  .glitch span:first-child {
    animation: glitch 500ms infinite;
    clip-path: polygon(0 0, 100% 0, 100% 35%, 0 35%);
    transform: translate(-0.04em, -0.03em);
    opacity: 0.75;
  }

  .glitch span:last-child {
    animation: glitch 375ms infinite;
    clip-path: polygon(0 65%, 100% 65%, 100% 100%, 0 100%);
    transform: translate(0.04em, 0.03em);
    opacity: 0.75;
  }

  @keyframes glitch {
    0% {
      text-shadow: 0.05em 0 0 #00fffc, -0.03em -0.04em 0 #fc00ff,
        0.025em 0.04em 0 #fffc00;
    }
    15% {
      text-shadow: 0.05em 0 0 #00fffc, -0.03em -0.04em 0 #fc00ff,
        0.025em 0.04em 0 #fffc00;
    }
    16% {
      text-shadow: -0.05em -0.025em 0 #00fffc, 0.025em 0.035em 0 #fc00ff,
        -0.05em -0.05em 0 #fffc00;
    }
    49% {
      text-shadow: -0.05em -0.025em 0 #00fffc, 0.025em 0.035em 0 #fc00ff,
        -0.05em -0.05em 0 #fffc00;
    }
    50% {
      text-shadow: 0.05em 0.035em 0 #00fffc, 0.03em 0 0 #fc00ff,
        0 -0.04em 0 #fffc00;
    }
    99% {
      text-shadow: 0.05em 0.035em 0 #00fffc, 0.03em 0 0 #fc00ff,
        0 -0.04em 0 #fffc00;
    }
    100% {
      text-shadow: -0.05em 0 0 #00fffc, -0.025em -0.04em 0 #fc00ff,
        -0.04em -0.025em 0 #fffc00;
    }
  }
</style>
