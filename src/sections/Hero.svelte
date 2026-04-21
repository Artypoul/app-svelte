<script>
  export let metrics = [];
</script>

<section class="hero">
  <div class="container hero__content">
    <p class="hero__eyebrow">Svelte + Timeweb Cloud</p>
    <h1>Запускайте интерфейсы уровня продакшн за часы, а не недели</h1>
    <p class="hero__description">
      Архитектура, компоненты и адаптивная вёрстка для экранов от 1920 до 1327px —
      всё уже собрано в одном проекте.
    </p>

    <div class="hero__actions">
      <button>Начать бесплатно</button>
      <a href="#features">Смотреть возможности</a>
    </div>

    <ul class="hero__metrics">
      {#each metrics as metric}
        <li>
          <p>{metric.value}</p>
          <span>{metric.label}</span>
        </li>
      {/each}
    </ul>
  </div>
</section>

<style>
  .hero {
    padding: clamp(56px, 6vw, 112px) 0 clamp(72px, 8vw, 120px);
    background:
      radial-gradient(circle at 10% 20%, rgba(131, 108, 255, 0.16), transparent 40%),
      radial-gradient(circle at 90% 10%, rgba(49, 216, 192, 0.16), transparent 30%);
  }

  h1 {
    max-width: 850px;
    font-size: var(--text-display);
    letter-spacing: -0.04em;
    line-height: 1.03;
    margin: 16px 0 22px;
  }

  .hero__eyebrow {
    display: inline-flex;
    padding: 8px 14px;
    border-radius: 999px;
    background: rgba(131, 108, 255, 0.16);
    color: var(--color-accent);
    margin: 0;
    font-size: var(--text-xs);
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.08em;
  }

  .hero__description {
    max-width: 660px;
    color: var(--color-text-muted);
    font-size: var(--text-md);
    line-height: 1.5;
    margin: 0 0 28px;
  }

  .hero__actions {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: clamp(30px, 4vw, 48px);
  }

  button {
    border: none;
    border-radius: 14px;
    background: var(--color-accent);
    color: #fff;
    font-size: var(--text-sm);
    font-weight: 600;
    padding: 14px 22px;
  }

  a {
    color: var(--color-text);
    text-decoration: none;
    font-size: var(--text-sm);
    font-weight: 600;
  }

  .hero__metrics {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 16px;
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .hero__metrics li {
    border: 1px solid var(--color-border);
    border-radius: 18px;
    background: var(--color-surface);
    padding: 20px;
  }

  .hero__metrics p {
    margin: 0;
    font-weight: 700;
    font-size: clamp(1.5rem, 1.5vw, 2rem);
  }

  .hero__metrics span {
    color: var(--color-text-muted);
    font-size: var(--text-xs);
  }

  @media (max-width: 1327px) {
    .hero__metrics {
      grid-template-columns: 1fr;
    }
  }
</style>
