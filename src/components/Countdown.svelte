<script>
  import { onMount } from 'svelte';
  import { writable } from 'svelte/store';

  const timeLeft = writable({ days: 0, hours: 0, minutes: 0, seconds: 0 });

  // Set event date once
  const eventDate = new Date();
  eventDate.setDate(eventDate.getDate() + 1);
  eventDate.setHours(23, 59, 59, 999); // Set event time to end of the next day

  let timer;

  function calculateTimeLeft() {
    const now = new Date();
    const difference = eventDate - now;

    if (difference > 0) {
      timeLeft.set({
        days: Math.floor(difference / (1000 * 60 * 60 * 24)),
        hours: Math.floor((difference / (1000 * 60 * 60)) % 24),
        minutes: Math.floor((difference / (1000 * 60)) % 60),
        seconds: Math.floor((difference / 1000) % 60),
      });
    } else {
      timeLeft.set({ days: 0, hours: 0, minutes: 0, seconds: 0 });
      clearInterval(timer);
    }
  }

  onMount(() => {
    calculateTimeLeft();
    timer = setInterval(calculateTimeLeft, 1000);
    return () => clearInterval(timer);
  });
</script>

<div class="countdown-timer">
  {#each Object.entries($timeLeft) as [key, value]}
    <div class="time-box">
      <span class="time">{value}</span>
      <span class="label">{key.charAt(0).toUpperCase() + key.slice(1)}</span>
    </div>
  {/each}
</div>

<style>
  .countdown-timer {
    display: flex;
    justify-content: center;
    gap: 1rem;
    font-family: 'Arial', sans-serif;
  }
  .time-box {
    text-align: center;
    background-color: #6e8efb;
    color: white;
    padding: 1rem;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    min-width: 50px;
  }
  .time {
    font-size: 2rem;
    font-weight: bold;
  }
  .label {
    font-size: 1rem;
  }
</style>
