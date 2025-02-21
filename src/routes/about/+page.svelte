<main>
  <section class="about">
    <div class="row card">
      <div class="about-image-container">
        <img src="/tech.jpg" alt="Tech Conference" class="about-image" />
      </div>
      <div class="about-text">
        <h1>About Tech Conference 2023</h1>
        <p>Welcome to the Tech Conference 2023, the premier event for tech enthusiasts. Join us for an exciting lineup of speakers, workshops, and networking opportunities. Whether you're a seasoned professional or just starting out, there's something for everyone at Tech Conference 2023.</p>
        <p>This year, we are bringing together the brightest minds in technology to share their knowledge and inspire the next generation of innovators. Our conference will feature keynote speeches, panel discussions, and interactive sessions that cover a wide range of topics, from artificial intelligence to cybersecurity.</p>
      </div>
    </div>
    <div class="row reverse card">
      <div class="about-image-container">
        <img src="/speaker.jpg" alt="Speakers" class="about-image" />
      </div>
      <div class="about-text">
        <h2>Our Speakers</h2>
        <p>Our speakers are industry leaders and innovators who will share their insights and experiences. Learn from the best and get inspired by their stories. Our lineup includes CEOs, CTOs, and thought leaders from top tech companies, as well as renowned researchers and academics.</p>
        <p>Each speaker brings a unique perspective and a wealth of knowledge to the conference. They will discuss the latest trends and developments in technology, share their experiences, and provide valuable advice for professionals at all stages of their careers.</p>
      </div>
    </div>
    <div class="row card">
      <div class="about-image-container">
        <img src="/workshop.jpg" alt="Workshops" class="about-image" />
      </div>
      <div class="about-text">
        <h2>Workshops</h2>
        <p>Participate in hands-on workshops and gain practical skills. Our workshops cover a wide range of topics, from coding to project management. Whether you're looking to learn a new programming language, improve your project management skills, or explore the latest tools and technologies, our workshops have something for you.</p>
        <p>Led by experienced instructors and industry experts, our workshops provide a supportive and interactive learning environment. You'll have the opportunity to work on real-world projects, collaborate with other participants, and receive personalized feedback and guidance.</p>
      </div>
    </div>
    <div class="row reverse card">
      <div class="about-image-container">
        <img src="/network.jpg" alt="Networking" class="about-image" />
      </div>
      <div class="about-text">
        <h2>Networking Opportunities</h2>
        <p>Connect with like-minded professionals and expand your network. Our conference provides ample opportunities for networking and collaboration. From informal meetups and social events to structured networking sessions, you'll have plenty of chances to meet new people, exchange ideas, and build valuable relationships.</p>
        <p>Networking is a key part of the Tech Conference experience. Whether you're looking to find a mentor, explore new career opportunities, or simply connect with others who share your interests, our conference offers a welcoming and inclusive environment for all attendees.</p>
      </div>
    </div>
  </section>
</main>

<style>
  main {
    font-family: 'Arial', sans-serif;
    padding: 2rem;
  }
  .about {
    max-width: 1200px;
    margin: 0 auto;
  }
  .row {
    display: flex;
    align-items: stretch;
    margin-bottom: 3rem;
    background: linear-gradient(135deg, #6e8efb, #a777e3);
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 4px 8px var(--card-shadow-color);
  }
  .row.reverse {
    flex-direction: row-reverse;
  }
  .about-image-container {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    border-radius: 8px;
  }
  .about-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .about-text {
    flex: 1;
    padding: 0 2rem;
    color: white;
  }
  .about h1, .about h2 {
    font-size: 2.2rem;
    margin-bottom: 1rem;
    color: white;
    font-weight: bold;
  }
  .about p {
    font-size: 1.1rem;
    line-height: 1.6;
    color: white;
    margin-bottom: 1.5rem;
  }
  @media (max-width: 768px) {
    .row {
      flex-direction: column;
      text-align: center;
    }
    .about-text {
      padding: 0 0.2rem;
    }
    .row.reverse {
      flex-direction: column;
    }
    .about-image-container {
      width: 100%;
      margin-bottom: 2rem;
    }
    .about h1, .about h2 {
      font-size: 2rem;
    }
  }
</style>
