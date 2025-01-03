<script>
  export let open = false;
</script>

<aside class:open class="sidebar">
  <nav class="p-4">
    <div class="navbar-item">
      <a href="/">
        <img
          class="navbar-icon"
          src="icons/dashboard-line.svg"
          alt="Dashboard view"
        />
        <p>Dashboard</p>
      </a>
    </div>
    <div class="navbar-item">
      <a href="/">
        <img class="navbar-icon" src="icons/bar-chart.svg" alt="Charts view" />
        <p>Analytics</p>
      </a>
    </div>
    <div class="navbar-item">
      <a href="/">
        <img class="navbar-icon" src="icons/alert.svg" alt="Alerts view" />
        <p>Alerts</p>
      </a>
    </div>
    <div class="navbar-item">
      <a href="/">
        <img
          class="navbar-icon"
          src="icons/report-analytics.svg"
          alt="Reporting analytics"
        />
        <p>Reporting Statistics</p>
      </a>
    </div>
    <div class="navbar-item">
      <a href="/">
        <img class="navbar-icon" src="icons/globe.svg" alt="Global view" />
        <p>Global</p>
      </a>
    </div>
    <hr class="divider" />
    <div class="navbar-item">
      <a href="/">
        <img
          class="navbar-icon"
          src="icons/settings-outline.svg"
          alt="Settings"
        />
        <p>Settings</p>
      </a>
    </div>
    <div class="navbar-item">
      <a href="/">
        <img
          class="navbar-icon"
          src="icons/bug-report.svg"
          alt="Report a bug"
        />
        <p>Report a bug</p>
      </a>
    </div>
    <div class="navbar-item">
      <a href="/">
        <img class="navbar-icon" src="icons/logout.svg" alt="Log out" />
        <p>Log out</p>
      </a>
    </div>
  </nav>
</aside>

<style>
  .sidebar {
    position: absolute;
    height: 100%;
    background-color: var(--sidebar-bg-color, #f8f9fa);
    width: 80px;
    transition: width 0.1s ease;
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid var(--sidebar-border-color, #ccc);
    top: 0;
  }

  .open {
    top: 0;
  }

  .sidebar:hover {
    width: 350px;
  }

  .navbar-item {
    margin: 1rem 0;
    display: flex;
    align-items: center;
  }

  .navbar-item a {
    display: flex;
    align-items: center;
    color: var(--primary-color, #333);
    padding: 0.5rem;
    transition: background-color 0.1s ease;
    width: 100%;
  }

  .p-4 {
    margin-top: 2rem;
  }

  .navbar-icon {
    width: 24px;
    height: 24px;
    margin-right: 16px;
  }

  .navbar-item p {
    opacity: 0;
    transition: opacity 0.1s ease;
    font-weight: var(--nav-font-weight);
  }

  .divider {
    margin: 3rem 0;
    border: 0;
    border-top: 1px solid #ddd;
  }

  @media (max-width: 767px) {
    .sidebar {
      width: 100%!important;
      top: -100%;
      transition: top 0.1s ease-in-out;
      border-right: none;
    }

    .navbar-item p {
      opacity: 1;
    }

    .open {
      top: 0;
    }
  }
  
  @media (min-width: 768px) {
    .navbar-item a:hover {
      color: var(--accent-color);
    }

    .navbar-item a:hover img {
      filter: brightness(0) saturate(100%) invert(41%) sepia(13%)
        saturate(5931%) hue-rotate(333deg) brightness(93%) contrast(95%);
    }

    .sidebar:hover .navbar-item p {
      opacity: 1;
    }
  }
</style>
