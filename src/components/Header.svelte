<script>
  export let navItems = [];
</script>

<header class="header">
  <div class="container header__inner">
    <a class="brand" href="/">TW</a>

    <ul class="nav-list">
      {#each navItems as item}
        <li><a href="/">{item}</a></li>
      {/each}
    </ul>

    <div class="header__actions">
      <button class="ghost">Войти</button>
      <button class="accent">Запустить</button>
    </div>
  </div>
</header>

<style>
  .header {
    padding-top: 28px;
  }

  .header__inner {
    height: 72px;
    border-radius: 20px;
    background: #fff;
    border: 1px solid var(--line);
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 20px 0 24px;
  }

  .brand {
    width: 40px;
    height: 40px;
    border-radius: 12px;
    background: var(--brand);
    color: #fff;
    display: grid;
    place-items: center;
    text-decoration: none;
    font-weight: 700;
    font-size: 14px;
  }

  .nav-list {
    display: flex;
    gap: 28px;
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .nav-list a {
    text-decoration: none;
    color: var(--text-2);
    font-size: 14px;
    font-weight: 500;
  }

  .header__actions {
    display: flex;
    gap: 10px;
  }

  button {
    border-radius: 12px;
    border: 1px solid var(--line);
    height: 40px;
    padding: 0 16px;
    font-size: 14px;
    font-weight: 600;
    background: #fff;
  }

  .accent {
    background: var(--brand);
    color: #fff;
    border-color: var(--brand);
  }

  @media (max-width: 1327px) {
    .nav-list {
      gap: 14px;
    }

    .header__actions .ghost {
      display: none;
    }
  }
</style>
