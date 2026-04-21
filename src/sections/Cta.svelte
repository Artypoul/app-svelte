<section class="cta">
  <div class="container cta__inner">
    <div>
      <p>Готово к запуску</p>
      <h2>Соберите и выкатите Svelte приложение в Timeweb Cloud Apps</h2>
    </div>

    <button>Создать приложение</button>
  </div>
</section>

<style>
  .cta {
    padding-bottom: 92px;
  }

  .cta__inner {
    border: 1px solid var(--color-border);
    border-radius: 24px;
    background: linear-gradient(135deg, rgba(131, 108, 255, 0.2), rgba(49, 216, 192, 0.15));
    display: flex;
    justify-content: space-between;
    gap: 32px;
    align-items: center;
    padding: clamp(24px, 3vw, 38px);
  }

  p {
    margin: 0 0 8px;
    font-size: var(--text-xs);
    font-weight: 700;
    text-transform: uppercase;
    color: var(--color-accent);
  }

  h2 {
    margin: 0;
    max-width: 680px;
    font-size: clamp(1.5rem, 2.2vw, 2.4rem);
    letter-spacing: -0.02em;
  }

  button {
    border: 0;
    border-radius: 14px;
    padding: 14px 20px;
    font-size: var(--text-sm);
    font-weight: 600;
    background: var(--color-text);
    color: #fff;
    white-space: nowrap;
  }

  @media (max-width: 1327px) {
    .cta__inner {
      flex-direction: column;
      align-items: flex-start;
    }
  }
</style>
