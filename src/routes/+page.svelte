<script>
  import sessionKit from "$lib/assets/images/kits/session-kit.svg"
  import contractKit from "$lib/assets/images/kits/contract-kit.svg"
  import accountKit from "$lib/assets/images/kits/account-kit.svg"
  // import VisionBoard from "$lib/components/VisionBoard.svelte"
  import reactIcon from "$lib/assets/icons/react.svg"
  import javascriptIcon from "$lib/assets/icons/javascript.svg"
  import vueIcon from "$lib/assets/icons/vue.svg"
  import nodeIcon from "$lib/assets/icons/node.svg"
</script>

<svelte:head>
  <style>
    /* prettier-ignore */
    body[data-theme="light"] {
      --footer-background: white;
      --page-background: 
      linear-gradient(
            180deg,
            #494e62 0%,
            #7be7ce 50rem,
            #b2f2e1 60rem,
            #f4faf4 70rem,
            #f4faf4 90%,
            hsl(120, 37%, 99%) 100%
          ) no-repeat;
    }

    /* prettier-ignore */
    body[data-theme="dark"] {
      --footer-background: hsl(228, 21%, 10%);
      --header-background: var(--wharf-blue); /* #494E62 */
      --header-background-transparent: #494E6200;
      --page-background: 
      linear-gradient(180deg, 
      hsl(166deg 69% 69%) 0%,
      hsl(172deg 31% 56%) 8rem,
      hsl(189deg 18% 44%) 20rem,
      hsl(228deg 15% 34%) 30rem,
      hsl(228deg 15% 28%) 40rem,
      hsl(228deg 16% 23%) 60rem,
      hsl(229deg 17% 18%) 80rem,
      hsl(229deg 17% 18%) 90%,
      hsl(229deg 17% 10%) 100%
      ) no-repeat;
    }

    body {
      /* Remove default gap to allow elements in <main> to overflow */
      --body-gap: 0;
    }

    .page {
      --page-padding-inline: 0;
    }
  </style>
</svelte:head>

<main class="stack">
  <section class="hero">
    <div class="box stack center">
      <h1>Modular SDK for Antelope Web Apps</h1>
      <p>
        Wharf provides a fast and flexible way to build web3 projects on blockchains like EOS,
        Telos, WAX, and UX.
      </p>
      <a href="/guides" class="button">Start Building Today</a>
    </div>
  </section>

  <section class="kits | full-bleed">
    <div class="images">
      <div class="account kit">
        <a href="/kits/account">
          <img src={accountKit} alt="account kit icon" />
        </a>
      </div>
      <div class="contract kit">
        <a href="/kits/contract">
          <img src={contractKit} alt="contract kit icon" />
        </a>
      </div>
      <div class="session kit">
        <a href="/kits/session">
          <img src={sessionKit} alt="session kit icon" />
        </a>
      </div>
    </div>

    <div class="launch | stack">
      <h2>What will you launch with Wharf?</h2>
      <p>
        Whether you want to create a wallet, mint NFTs, design a DeFi protocol, or build something
        entirely new: the days of clunky, limited blockchain SDKs are over! Wharf’s modular and
        user-focused approach saves development time and effort, helping to turn your ideas into
        reality.
      </p>
      <a href="/kits" class="button">Learn About the Kits</a>
    </div>
  </section>

  <section class="tools | switcher">
    <div class="frameworks card | box">
      <p class="visually-hidden">Supported Frameworks</p>
      <div class="cluster">
        <img src={reactIcon} alt="React" loading="lazy" />
        <img src={javascriptIcon} alt="Javascript" loading="lazy" />
        <img src={vueIcon} alt="Vue" loading="lazy" />
        <img src={nodeIcon} alt="NodeJS" loading="lazy" />
      </div>
    </div>
    <div class="box stack left">
      <h3>Get started with your favorite tools.</h3>
      <p>
        Wharf is designed to work with all Javascript frameworks. So whether you prefer to code in
        Vue, React, Svelte, Typescript, or NodeJS, you can start building today.
      </p>
      <p>Check back soon for Starter Kits in your favorite framework!</p>
      <!-- <a href="/docs" class="button">Check It Out</a> -->
    </div>
  </section>

  <section class="contract | box stack center">
    <h2>Want to keep up with the latest Wharf developments?</h2>
    <p>Check out our blog for regular video updates and technical previews.</p>
    <a href="/blog" class="button">Go to the Blog</a>
  </section>

  <section class="cards | switcher">
    <div class="card | box stack left">
      <h3>UX your users will love.</h3>
      <p>
        Want to provide a professional user experience, as fast as possible? Wharf provides an
        out-of-the-box UI Renderer that was created by a professional UX designer and covers
        multiple common user scenarios.
      </p>
      <a href="/kits/session" class="button">Learn More About the Session Kit</a>
    </div>
    <div class="card | box stack left">
      <h3>Build on the most responsive blockchains.</h3>
      <p>
        The Antelope framework is behind some of the fastest, most secure, and user-friendly Web3
        products and services. Together the EOS, Telos, WAX and UX networks reliably fulfill
        millions of transactions per day.
      </p>
      <a href="https://antelope.io/" class="button">Learn More About Antelope</a>
    </div>
  </section>

  <section class="box stack center">
    <h2>Ready to dive in? Wharf's docs have everything you need to start building.</h2>
    <p>Check out our blog for regular video updates and technical previews.</p>
    <a href="/docs" class="button">Go to Documentation</a>
  </section>

  <!-- <section class="vision | full-bleed">
    <VisionBoard />
  </section> -->
</main>

<style>
  .switcher {
    --threshold: 768px;
  }

  main {
    /* Re-insert default gap via padding */
    padding-block-start: var(--space-xl-2xl);
    max-inline-size: revert;
    overflow: hidden;
    gap: var(--space-3xl-4xl);
  }

  :where(h1, h2, h3, p) {
    /* Nicer wrapping in Chrome */
    text-wrap: balance;
  }

  main > * {
    /* Allows individual sections to break out from the max-inline-size */
    max-inline-size: var(--max-inline-size);
    margin-inline: auto;
    width: calc(100% - var(--space-s) * 2);
  }

  .hero {
    padding-block-start: var(--space-6xl);
    /* padding-block-start: 15vh; */
    padding-block-end: var(--space-4xl-5xl);
    /* padding-block-end: 15vh; */
    display: grid;
    place-items: center;
    position: relative;
  }

  .hero::before {
    content: url("/src/lib/assets/images/group-2554.svg");
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: -1;
    opacity: 0.6;
  }

  :global([data-theme="dark"]) .hero::before {
    content: url("/src/lib/assets/images/group-2554-dark.svg");
  }

  .hero .stack {
    gap: var(--space-l);
  }

  .hero h1 {
    font-size: var(--fs-6);
    color: white;
    max-width: 20ch;
  }

  .hero p {
    font-size: var(--fs-1);
    font-weight: 500;
    color: white;
    max-width: 35ch;
  }

  .images {
    display: grid;
    grid-template-columns: 1fr auto auto auto 1fr;
    grid-template-rows: repeat(3, 1fr);
    column-gap: var(--space-l);
    position: relative;
    margin-bottom: var(--space-xl);
  }

  .images::before {
    content: "";
    position: absolute;
    inset: 0;
    z-index: -1;
    top: calc(var(--space-m) * -1);
    background-image: url("/src/lib/assets/images/Frame-2591.webp");
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
  }

  .kit {
    display: grid;
    position: relative;
  }

  .kit img {
    transition: transform 200ms ease;
  }

  .kit a:hover img {
    transform: translateY(-0.5rem);
  }

  .account.kit {
    grid-column: 2 / 3;
    grid-row: 2 / 4;
    justify-items: end;
  }

  .contract.kit {
    grid-column: 3 / 4;
    grid-row: 1 / 3;
    justify-items: center;
  }

  .session.kit {
    grid-column: 4 / 5;
    grid-row: 2 / 4;
  }

  .center {
    align-items: center;
    text-align: center;
  }

  .left {
    align-items: flex-start;
  }

  .full-bleed {
    width: 100%;
  }

  .card {
    --padding: var(--space-l-xl);
    background-color: var(--theme-surface7);
    border-radius: var(--space-l);
  }

  div.launch {
    background: linear-gradient(180deg, transparent 0, var(--theme-surface7) 15rem);
    width: 100%;
    text-align: center;
    align-items: center;
    padding-block: var(--space-xl);
  }

  div.launch p {
    margin-inline: var(--space-s);
    max-width: 65ch;
  }

  section.tools {
    --padding: var(--space-l);
    gap: var(--space-l);
    width: calc(100% - var(--space-s) * 2);
    margin-inline: auto;
  }

  .frameworks {
    color: white;
    background: url("/src/lib/assets/images/9adffb9d8509834788bd5a77f798bc5b.webp");
    background-size: cover;
    background-repeat: no-repeat;
  }

  .frameworks.card {
    display: grid;
    place-content: center;
    text-align: center;
    gap: var(--space-m);
  }

  .frameworks .cluster {
    justify-content: center;
    max-width: 35ch;
  }

  .frameworks p {
    font-family: var(--ff-heading);
    font-weight: 600;
  }

  section.tools h3 {
    font-size: var(--fs-3);
  }

  section.contract h4 {
    font-size: var(--fs-3);
  }

  section.cards {
    position: relative;
  }

  section.cards::before {
    content: url("/src/lib/assets/images/squiggle-1.svg");
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -40%);
    z-index: -1;
    opacity: 0.1;
  }

  :global([data-theme="dark"]) section.cards::before {
    opacity: 1;
  }

  @media (min-width: 768px) {
    .images::before,
    .images::after {
      --kit-bg-source: url("/src/lib/assets/images/Frame-2591.webp");
      content: var(--kit-bg-source);
      position: absolute;
      inset: revert;
      background: none;
      top: 50%;
      left: 50%;
      z-index: -1;
    }

    .images::before {
      transform: translate(-140%, -30%);
    }

    .images::after {
      transform: translate(40%, -30%);
    }

    :global([data-theme="dark"]) .images::before,
    :global([data-theme="dark"]) .images::after {
      --kit-bg-source: url("/src/lib/assets/images/Frame-2650.webp");
    }

    .contract.kit::before {
      content: url("/src/lib/assets/images/Frame-2588.webp");
      position: absolute;
      top: -25%;
      z-index: -1;
    }

    :global([data-theme="dark"]) .contract.kit::before {
      content: url("/src/lib/assets/images/Frame-2588-dark.webp");
    }

    div.launch {
      border-radius: 0 0 var(--space-l) var(--space-l);
      padding-block: var(--space-2xl-3xl);
    }

    .full-bleed {
      border-radius: var(--space-l);
      width: calc(100% - var(--space-s) * 2);
    }

    section.tools {
      --padding: var(--space-xl-2xl);
    }
  }
</style>
