<section class="cta">
  <div class="container box">
    <div>
      <p>Ready for launch</p>
      <h2>Собранный Svelte-экран в продуктовой структуре Timeweb</h2>
      <span>Подходит как стартовая база для подключения API и дальнейшей детализации по макету.</span>
    </div>
    <button>Запустить проект</button>
  </div>
</section>

<style>
  .cta {
    padding: 0 0 64px;
  }

  .box {
    background: linear-gradient(120deg, #131736 0%, #1f2250 54%, #2f3480 100%);
    color: #fff;
    border-radius: 24px;
    padding: 34px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 24px;
    border: 1px solid #34398c;
  }

  p {
    margin: 0 0 10px;
    text-transform: uppercase;
    font-size: 11px;
    letter-spacing: 0.08em;
    color: #99a6ff;
    font-weight: 700;
  }

  h2 {
    margin: 0 0 8px;
    max-width: 760px;
    font-size: 34px;
    line-height: 1.1;
  }

  span {
    color: #d6dbff;
    font-size: 14px;
  }

  button {
    border: 0;
    border-radius: 12px;
    background: #fff;
    color: #171a2b;
    height: 46px;
    padding: 0 18px;
    font-weight: 700;
    white-space: nowrap;
  }

  @media (max-width: 1327px) {
    .box {
      flex-direction: column;
      align-items: flex-start;
    }
  }
</style>
