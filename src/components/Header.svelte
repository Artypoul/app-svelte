<script>
  export let navItems = [];
</script>

<header class="header">
  <div class="container header__inner">
    <a class="brand" href="/">Timeweb UI</a>

    <nav aria-label="Основная навигация">
      <ul class="nav-list">
        {#each navItems as item}
          <li><a href="/">{item}</a></li>
        {/each}
      </ul>
    </nav>

    <button class="header__button">Войти</button>
  </div>
</header>

<style>
  .header {
    position: sticky;
    top: 0;
    z-index: 10;
    backdrop-filter: blur(10px);
    background: color-mix(in srgb, var(--color-bg) 90%, transparent);
    border-bottom: 1px solid var(--color-border);
  }

  .header__inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    min-height: 88px;
  }

  .brand {
    font-size: var(--text-lg);
    color: var(--color-text);
    font-weight: 700;
    text-decoration: none;
  }

  .nav-list {
    display: flex;
    gap: clamp(16px, 2vw, 32px);
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .nav-list a {
    color: var(--color-text-muted);
    text-decoration: none;
    font-size: var(--text-sm);
  }

  .header__button {
    background: var(--color-accent);
    color: #fff;
    border: 0;
    border-radius: 14px;
    padding: 12px 18px;
    font-size: var(--text-sm);
    font-weight: 600;
  }

  @media (max-width: 1327px) {
    .nav-list {
      display: none;
    }
  }
</style>
