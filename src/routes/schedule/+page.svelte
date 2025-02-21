<script>
  const sessions = [
    { date: '25-02-2025', time: '10:00 AM', topic: 'Opening Keynote', speaker: 'John Doe' },
    { date: '25-02-2025', time: '11:00 AM', topic: 'Future of AI', speaker: 'Jane Smith' },
    { date: '25-02-2025', time: '01:00 PM', topic: 'Cybersecurity Trends', speaker: 'Alice Johnson' },
    { date: '25-02-2025', time: '02:00 PM', topic: 'Blockchain Technology', speaker: 'Bob Brown' },
    { date: '26-02-2025', time: '10:00 AM', topic: 'Cloud Computing', speaker: 'Charlie Davis' },
    { date: '26-02-2025', time: '11:00 AM', topic: 'Quantum Computing', speaker: 'Diana Evans' },
    { date: '26-02-2025', time: '01:00 PM', topic: 'IoT Innovations', speaker: 'Eve Foster' },
    { date: '26-02-2025', time: '02:00 PM', topic: 'AR/VR Applications', speaker: 'Frank Green' },
  ];
</script>

<main>
  <h1>Schedule</h1>
  <table>
    <thead>
      <tr>
        <th>Date</th>
        <th>Time</th>
        <th>Topic</th>
        <th>Speaker</th>
      </tr>
    </thead>
    <tbody>
      {#each sessions as session}
        <tr>
          <td>{session.date}</td>
          <td>{session.time}</td>
          <td>{session.topic}</td>
          <td>{session.speaker}</td>
        </tr>
      {/each}
    </tbody>
  </table>

  <div class="row card">
    <div class="about-image-container">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d12607.609978242193!2d144.9416558871582!3d-37.81575279999999!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6ad65d4f13389fef%3A0x97082cad1d1c34d8!2sQ%20Events%20-%20Event%20Space%20Melbourne%2C%20Wedding%20Venue%20%26%20Corporate%20Events%20Venue!5e0!3m2!1sen!2sau!4v1740169280521!5m2!1sen!2sau" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
    <div class="about-text">
      <h2>Venue: Q Events</h2>
      <p>The Tech Conference 2025 will be held at Q Events, Melbourne, Australia. Join us at this iconic location for an unforgettable experience.</p>
      <h3>Instructions</h3>
      <ul>
        <li>Bring your passes with you for entry.</li>
        <li>No dress code.</li>
        <li>Refreshments, food, and drinks will be provided.</li>
      </ul>
      <h3>Accessibility</h3>
      <ul>
        <li>Wheelchair-accessible car park</li>
        <li>Wheelchair-accessible entrance</li>
        <li>Wheelchair-accessible seating</li>
        <li>Wheelchair-accessible toilet</li>
      </ul>
      <h3>Amenities</h3>
      <ul>
        <li>Toilet</li>
        <li>Free WiFi</li>
      </ul>
      <h3>Crowd</h3>
      <ul>
        <li>LGBTQ+ friendly</li>
        <li>Transgender safe space</li>
      </ul>
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
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 0 auto;
    box-shadow: 0 4px 8px var(--card-shadow-color);
    border-radius: 8px;
    overflow: hidden;
    background: var(--card-background-color);
  }
  th, td {
    border: 1px solid #ddd;
    padding: 12px;
    text-align: left;
    color: var(--text-color);
  }
  th {
    background-color: var(--primary-color);
    color: white;
    font-weight: bold;
  }
  tr:nth-child(even) {
    background-color: rgba(255, 255, 255, 0.1);
  }
  .row {
    display: flex;
    align-items: stretch;
    margin-top: 3rem;
    background: var(--card-background-color);
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 4px 8px var(--card-shadow-color);
  }
  .about-image-container {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    border-radius: 8px;
  }
  .about-text {
    flex: 1;
    padding: 0 2rem;
    color: var(--text-color);
  }
  @media (max-width: 768px) {
    .row {
      flex-direction: column;
      text-align: center;
    }
    .about-image-container {
      width: 100%;
      margin-bottom: 2rem;
    }
  }
</style>
