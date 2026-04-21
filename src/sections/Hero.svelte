<script>
  export let metrics = [];
</script>

<section class="hero">
  <div class="container hero__grid">
    <div>
      <p class="badge">Svelte starter</p>
      <h1>Сверстано под макет для брейкпоинта 1327px</h1>
      <p class="lead">Чистая архитектура, модульные секции и дизайн-токены — готовая база для продуктового интерфейса.</p>

      <div class="actions">
        <button>Создать приложение</button>
        <a href="#features">Подробнее</a>
      </div>

      <ul class="metrics">
        {#each metrics as metric}
          <li>
            <strong>{metric.value}</strong>
            <span>{metric.label}</span>
          </li>
        {/each}
      </ul>
    </div>

    <aside class="preview" aria-label="Превью интерфейса">
      <div class="preview__top"></div>
      <div class="preview__chart"></div>
      <div class="preview__bottom"></div>
    </aside>
  </div>
</section>

<style>
  .hero {
    padding: 24px 0 56px;
  }

  .hero__grid {
    display: grid;
    grid-template-columns: 1fr 470px;
    gap: 24px;
  }

  h1 {
    margin: 14px 0 14px;
    max-width: 720px;
    font-size: 58px;
    line-height: 1;
    letter-spacing: -0.03em;
  }

  .badge {
    margin: 0;
    display: inline-block;
    padding: 8px 12px;
    border-radius: 100px;
    background: #ece8ff;
    color: var(--brand);
    font-size: 12px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.08em;
  }

  .lead {
    margin: 0;
    max-width: 620px;
    color: var(--text-2);
    font-size: 18px;
    line-height: 1.5;
  }

  .actions {
    display: flex;
    align-items: center;
    gap: 14px;
    margin: 26px 0;
  }

  button {
    border: 0;
    background: var(--brand);
    color: #fff;
    border-radius: 14px;
    height: 48px;
    padding: 0 20px;
    font-size: 15px;
    font-weight: 600;
  }

  a {
    color: var(--text-1);
    text-decoration: none;
    font-weight: 600;
    font-size: 15px;
  }

  .metrics {
    list-style: none;
    padding: 0;
    margin: 0;
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 12px;
    max-width: 720px;
  }

  .metrics li {
    background: #fff;
    border: 1px solid var(--line);
    border-radius: 16px;
    padding: 14px;
    display: grid;
    gap: 6px;
  }

  strong {
    font-size: 26px;
    line-height: 1;
  }

  span {
    color: var(--text-2);
    font-size: 12px;
  }

  .preview {
    border-radius: 24px;
    padding: 16px;
    background: linear-gradient(161deg, #2e2666 2%, #43328f 40%, #271f5b 100%);
    border: 1px solid #5448a0;
    display: grid;
    gap: 12px;
    min-height: 420px;
  }

  .preview > div {
    border-radius: 14px;
    background: rgba(255, 255, 255, 0.12);
    border: 1px solid rgba(255, 255, 255, 0.2);
  }

  .preview__top {
    height: 110px;
  }

  .preview__chart {
    flex: 1;
    min-height: 160px;
  }

  .preview__bottom {
    height: 84px;
  }

  @media (max-width: 1327px) {
    .hero__grid {
      grid-template-columns: 1fr;
    }

    h1 {
      font-size: 46px;
    }

    .preview {
      min-height: 320px;
    }
  }
</style>
