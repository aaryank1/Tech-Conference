<script>
  import { Nav, NavItem, NavLink } from 'sveltestrap';
  import { onMount } from 'svelte';
  let isOpen = false;
  let isDarkMode = false;

  function toggleMenu() {
    isOpen = !isOpen;
  }

  function toggleTheme() {
    isDarkMode = !isDarkMode;
    document.documentElement.setAttribute('data-theme', isDarkMode ? 'dark' : 'light');
  }

  function closeMenu() {
    isOpen = false;
  }

  onMount(() => {
    const handleResize = () => {
      if (window.innerWidth > 768) {
        isOpen = false;
      }
    };
    window.addEventListener('resize', handleResize);
    return () => window.removeEventListener('resize', handleResize);
  });
</script>

<div class="navbar-wrapper">
  <div class="custom-navbar">
    <button class="menu-button" on:click={toggleMenu} aria-label="Toggle menu">
      <svg width="24" height="24" viewBox="0 0 24 24">
        <path fill="white" d="M3 6h18v2H3zm0 5h18v2H3zm0 5h18v2H3z"/>
      </svg>
    </button>
    
    <div class="nav-container" class:open={isOpen}>
      <Nav pills={true} class="custom-nav">
        <NavItem>
          <NavLink href="/" on:click={closeMenu}>Home</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/speakers" on:click={closeMenu}>Speakers</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/schedule" on:click={closeMenu}>Schedule</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/sponsors" on:click={closeMenu}>Sponsors</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/about" on:click={closeMenu}>About</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/contact" on:click={closeMenu}>Contact</NavLink>
        </NavItem>
      </Nav>
    </div>

    <button class="theme-toggle" on:click={toggleTheme} aria-label="Toggle theme">
      {#if isDarkMode}
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/>
        </svg>
      {:else}
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="12" cy="12" r="5"/>
          <line x1="12" y1="1" x2="12" y2="3"/>
          <line x1="12" y1="21" x2="12" y2="23"/>
          <line x1="4.22" y1="4.22" x2="5.64" y2="5.64"/>
          <line x1="18.36" y1="18.36" x2="19.78" y2="19.78"/>
          <line x1="1" y1="12" x2="3" y2="12"/>
          <line x1="21" y1="12" x2="23" y2="12"/>
          <line x1="4.22" y1="19.78" x2="5.64" y2="18.36"/>
          <line x1="18.36" y1="5.64" x2="19.78" y2="4.22"/>
        </svg>
      {/if}
    </button>
  </div>
</div>

<style>
  .navbar-wrapper {
    padding: 0 1rem;
    width: 100%;
    box-sizing: border-box;
  }

  .custom-navbar {
    background-color: var(--primary-color);
    padding: 1rem;
    border-radius: 8px;
    box-shadow: 0 4px 8px var(--card-shadow-color);
    margin-bottom: 2rem;
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    box-sizing: border-box;
  }

  .menu-button {
    display: none;
    background: none;
    border: none;
    cursor: pointer;
    padding: 0.5rem;
  }

  .theme-toggle {
    background: none;
    border: none;
    cursor: pointer;
    padding: 0.5rem;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: transform 0.2s;
  }

  .theme-toggle:hover {
    transform: scale(1.1);
  }

  .nav-container {
    flex: 1;
  }

  /* Style overrides for Sveltestrap components */
  :global(.custom-nav) {
    display: flex;
    flex-direction: row;
    justify-content: center;
    gap: 1rem;
    margin: 0;
    padding: 0;
  }

  :global(.custom-nav .nav-item) {
    list-style-type: none;
  }

  :global(.custom-nav .nav-link) {
    color: var(--text-color) !important;
    font-weight: bold;
    font-size: 1.2rem;
    text-decoration: none;
    transition: color 0.3s;
    padding: 0.5rem 1rem;
  }

  :global(.custom-nav .nav-link:hover) {
    color: #e0e0e0 !important;
  }

  @media (max-width: 768px) {
    .navbar-wrapper {
      padding: 0 0.5rem;
    }

    .menu-button {
      display: block;
    }

    .nav-container {
      display: none;
      width: 100%;
      position: absolute;
      top: 100%;
      left: 0;
      background-color: var(--primary-color);
      border-radius: 0 0 8px 8px;
      padding: 0.5rem;
      box-sizing: border-box;
      z-index: 1000;
    }

    .nav-container.open {
      display: block;
    }

    :global(.custom-nav) {
      flex-direction: column;
      align-items: stretch;
      padding: 0;
    }

    :global(.custom-nav .nav-item) {
      width: 100%;
    }

    :global(.custom-nav .nav-link) {
      text-align: center;
      display: block;
      padding: 0.75rem;
    }
  }
</style>