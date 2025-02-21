<script>
  import { Card, CardBody, CardTitle, CardText } from 'sveltestrap';
  const speakers = [
    { name: 'John Doe', title: 'CEO, TechCorp', bio: 'John has over 20 years of experience in the tech industry...', img: '/john.jpg' },
    { name: 'Jane Smith', title: 'CTO, Innovate Inc.', bio: 'Jane is a leading expert in AI and machine learning...', img: '/jane.jpg' },
    { name: 'Alice Johnson', title: 'Cybersecurity Specialist', bio: 'Alice has been working in cybersecurity for over a decade...', img: '/alice.jpeg' },
    { name: 'Bob Brown', title: 'Blockchain Developer', bio: 'Bob is a blockchain developer with extensive experience...', img: '/bob.jpeg' },
    { name: 'Charlie Davis', title: 'Cloud Computing Expert', bio: 'Charlie is a cloud computing expert with numerous certifications...', img: '/charlie.jpeg' },
    { name: 'Diana Evans', title: 'Quantum Computing Researcher', bio: 'Diana is a researcher in quantum computing...', img: '/diana.jpeg' },
    { name: 'Eve Foster', title: 'IoT Innovator', bio: 'Eve is an innovator in the field of Internet of Things...', img: '/eve.jpeg' },
    { name: 'Frank Green', title: 'AR/VR Developer', bio: 'Frank is a developer specializing in AR and VR applications...', img: '/frank.jpg' }
  ];
</script>

<main>
  <h1>Speakers</h1>
  <div class="grid">
    {#each speakers as speaker}
      <Card style="background: var(--card-background-color); border: none; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); border-radius: 8px; display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 1rem;">
        <img src={speaker.img} alt={speaker.name} class="speaker-img" />
        <CardBody style="text-align: center;">
          <CardTitle>{speaker.name}</CardTitle>
          <CardText>{speaker.title}</CardText>
          <CardText>{speaker.bio}</CardText>
        </CardBody>
      </Card>
    {/each}
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
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1rem;
  }
  .speaker-img {
    max-width: 100%;
    height: auto;
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 50%;
    margin-bottom: 1rem;
  }
</style>
