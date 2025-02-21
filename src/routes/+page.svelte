<script>
  import { Button } from 'sveltestrap';
  import Countdown from '../components/Countdown.svelte';
  import FeaturedSpeakers from '../components/FeaturedSpeakers.svelte';
</script>

<main>
  <section class="hero">
    <h1>Tech Conference 2025</h1>
    <p>The premier event for tech enthusiasts</p>
    <Button class="register-button" color="primary" style="font-size: 1.2rem; padding: 0.75rem 1.5rem; background-color: #ff9800; border: none; border-radius: 10px; color: white; cursor: pointer; transition: background-color 0.3s;">Register Now</Button>
  </section>

  <section class="countdown">
    <Countdown />
  </section>

  <section class="featured-speakers">
    <FeaturedSpeakers />
  </section>
</main>

<style>
  main {
    font-family: 'Arial', sans-serif;
  }
  .hero {
    text-align: center;
    padding: 4rem 2rem;
    background: linear-gradient(135deg, #6e8efb, #a777e3);
    color: white;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    margin-bottom: 2rem;
  }
  .hero h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
  }
  .hero p {
    font-size: 1.5rem;
    margin-bottom: 2rem;
  }
  .countdown, .featured-speakers {
    margin: 2rem 0;
  }
</style>
