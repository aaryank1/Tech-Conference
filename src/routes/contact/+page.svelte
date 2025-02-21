<script>
  let name = '';
  let email = '';
  let message = '';
  
  function handleSubmit() {
    // Handle form submission
    alert(`Message sent by ${name}`);
  }
</script>

<main>
  <h1>Contact Us</h1>
  <form on:submit|preventDefault={handleSubmit}>
    <div class="form-group">
      <label for="name">Name</label>
      <input id="name" type="text" bind:value={name} required />
    </div>
    <div class="form-group">
      <label for="email">Email</label>
      <input id="email" type="email" bind:value={email} required />
    </div>
    <div class="form-group">
      <label for="message">Message</label>
      <textarea id="message" bind:value={message} required></textarea>
    </div>
    <button type="submit">Send</button>
  </form>
  <div class="social-media">
    <a href="https://twitter.com/techconf" target="_blank">
      <img src="/x.jpg" alt="Twitter" class="social-icon" />
    </a>
    <a href="https://facebook.com/techconf" target="_blank">
      <img src="/facebook-logo.png" alt="Facebook" class="social-icon" />
    </a>
    <a href="https://www.linkedin.com/company/techconf" target="_blank">
      <img src="/linkedin-logo.png" alt="LinkedIn" class="social-icon" />
    </a>
    <a href="https://www.instagram.com/techconf" target="_blank">
      <img src="/instagram-logo.jpg" alt="Instagram" class="social-icon" />
    </a>
  </div>
</main>

<style>
  main {
    font-family: 'Arial', sans-serif;
    padding: 2rem;
    max-width: 600px;
    margin: 0 auto;
    background: var(--card-background-color);
    border-radius: 8px;
    box-shadow: 0 4px 8px var(--card-shadow-color);
  }
  h1 {
    text-align: center;
    margin-bottom: 2rem;
    font-size: 2.5rem;
    color: var(--text-color);
  }
  form {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  .form-group {
    display: flex;
    flex-direction: column;
  }
  label {
    font-weight: bold;
    margin-bottom: 0.5rem;
    color: var(--text-color);
  }
  input, textarea {
    padding: 0.75rem;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 1rem;
    background-color: var(--background-color);
    color: var(--text-color);
  }
  textarea {
    resize: vertical;
    min-height: 150px;
  }
  button {
    padding: 0.75rem;
    background-color: var(--primary-color);
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1rem;
    transition: background-color 0.3s;
  }
  button:hover {
    background-color: #5a7de0;
  }
  .social-media {
    margin-top: 2rem;
    text-align: center;
  }
  .social-media a {
    margin-right: 1rem;
    display: inline-block;
  }
  .social-icon {
    width: 35px;
    height: 35px;
    border-radius: 100%;
  }
</style>
