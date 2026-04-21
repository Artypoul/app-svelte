<script>
  export let cards = [];
</script>

<section class="features" id="features">
  <div class="container">
    <div class="features__heading">
      <p>Возможности</p>
      <h2>Базовая архитектура для масштабирования продукта</h2>
    </div>

    <div class="features__grid">
      {#each cards as card}
        <article>
          <h3>{card.title}</h3>
          <p>{card.text}</p>
        </article>
      {/each}
    </div>
  </div>
</section>

<style>
  .features {
    padding: 0 0 80px;
  }

  .features__heading {
    max-width: 760px;
    margin-bottom: 28px;
  }

  .features__heading p {
    margin: 0 0 10px;
    color: var(--color-accent);
    font-size: var(--text-xs);
    font-weight: 700;
    text-transform: uppercase;
  }

  .features__heading h2 {
    margin: 0;
    font-size: clamp(1.9rem, 2.6vw, 3rem);
    letter-spacing: -0.03em;
  }

  .features__grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 16px;
  }

  article {
    padding: 26px;
    background: var(--color-surface);
    border-radius: 18px;
    border: 1px solid var(--color-border);
  }

  h3 {
    margin: 0 0 10px;
    font-size: var(--text-lg);
  }

  article p {
    margin: 0;
    color: var(--color-text-muted);
    line-height: 1.5;
  }

  @media (max-width: 1327px) {
    .features__grid {
      grid-template-columns: 1fr;
    }
  }
</style>
