<script>
  export let metrics = [];
</script>

<section class="hero">
  <div class="container hero__grid">
    <div>
      <p class="badge">Svelte + Timeweb</p>
      <h1>Готовая вёрстка интерфейса для desktop брейкпоинта 1327px</h1>
      <p class="lead">Экран собран компонентно: шапка, герой, карточки, CTA и футер. Удобно масштабировать без потери консистентности.</p>

      <div class="actions">
        <button>Начать</button>
        <a href="#features">Возможности</a>
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
      <div class="topbar">
        <span></span><span></span><span></span>
      </div>
      <div class="mock-card card-a"></div>
      <div class="chart"></div>
      <div class="row">
        <div class="mock-card"></div>
        <div class="mock-card"></div>
      </div>
    </aside>
  </div>
</section>

<style>
  .hero {
    padding: 28px 0 60px;
  }

  .hero__grid {
    display: grid;
    grid-template-columns: 1fr 470px;
    gap: 24px;
    align-items: stretch;
  }

  h1 {
    margin: 14px 0;
    max-width: 760px;
    font-size: 56px;
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
    padding: 0 22px;
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
    background: linear-gradient(165deg, #2d2664 0%, #4f3f9f 45%, #2a225d 100%);
    border: 1px solid #5e54ab;
    display: grid;
    gap: 10px;
  }

  .topbar {
    height: 34px;
    border-radius: 10px;
    background: rgba(255, 255, 255, 0.15);
    border: 1px solid rgba(255, 255, 255, 0.2);
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 0 10px;
  }

  .topbar span {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.6);
  }

  .mock-card,
  .chart {
    border-radius: 12px;
    background: rgba(255, 255, 255, 0.13);
    border: 1px solid rgba(255, 255, 255, 0.2);
  }

  .card-a {
    height: 88px;
  }

  .chart {
    min-height: 190px;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.18), rgba(255, 255, 255, 0.07));
  }

  .row {
    display: grid;
    gap: 10px;
    grid-template-columns: 1fr 1fr;
  }

  .row .mock-card {
    height: 86px;
  }

  @media (max-width: 1327px) {
    .hero__grid {
      grid-template-columns: 1fr;
    }

    h1 {
      font-size: 44px;
    }
  }
</style>
