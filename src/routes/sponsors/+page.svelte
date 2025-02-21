<script>
  import { onMount } from 'svelte';

  const sponsors = [
    { tier: 'Gold', name: 'Microsoft', logo: '/microsoft.jpg', link: 'https://www.microsoft.com/en-in' },
    { tier: 'Gold', name: 'Google', logo: '/google.png', link: 'https://www.google.com/' },
    { tier: 'Silver', name: 'Amazon', logo: '/amazon.png', link: 'https://www.amazon.in/' },
    { tier: 'Silver', name: 'Meta', logo: '/meta.png', link: 'https://about.meta.com/' },
    { tier: 'Bronze', name: 'Disney', logo: '/disney.png', link: 'https://www.hotstar.com/' },
    { tier: 'Bronze', name: 'Netflix', logo: '/netflix.png', link: 'https://www.netflix.com/' },
    // ...more sponsors
  ];

  let sponsorsTrack;

  onMount(() => {
    const track = sponsorsTrack;
    const items = track.children;
    const totalItems = items.length;

    // Clone the items to create a seamless loop
    for (let i = 0; i < totalItems; i++) {
      track.appendChild(items[i].cloneNode(true));
    }
  });
</script>

<main>
  <h1>Sponsors</h1>
  <div class="sponsors-carousel">
    <div class="sponsors-track" bind:this={sponsorsTrack}>
      {#each sponsors as sponsor}
        <div class="sponsor">
          <a href={sponsor.link} target="_blank">
            <img src={sponsor.logo} alt={sponsor.name} />
            <p>{sponsor.name}</p>
          </a>
        </div>
      {/each}
    </div>
  </div>
</main>

<style>
  main {
    font-family: 'Arial', sans-serif;
    padding: 2rem;
  }
  h1 {
    text-align: center;
    margin-bottom: 2rem;
    font-size: 2.5rem;
    color: var(--text-color);
  }
  .sponsors-carousel {
    overflow: hidden;
    position: relative;
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
  }
  .sponsors-track {
    display: flex;
    animation: scroll 20s linear infinite;
  }
  .sponsor {
    flex: 0 0 auto;
    justify-content: center;
    align-items: center;
    width: 250px;
    text-align: center;
    padding: 1rem;
    margin: 0 1rem; /* Add margin to increase the distance between sponsors */
  }
  .sponsor img {
    max-width: 100%;
    height: auto;
    max-height: 100px;
    margin-bottom: 1rem;
  }
  .sponsor p {
    font-size: 1.2rem;
    font-weight: bold;
    color: var(--text-color);
  }
  @keyframes scroll {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-50%);
    }
  }
  @media (max-width: 768px) {
    .sponsor {
      justify-content: center;
      align-items: center;
      width: 100px;
    }
    .sponsors-track {
      animation-duration: 10s; /*Increase the speed for small screens */
    }
  }
</style>
