<script>
  export let cards = [];
</script>

<section class="features" id="features">
  <div class="container">
    <div class="head">
      <p>Что внутри</p>
      <h2>Архитектура под Timeweb-структуру проекта</h2>
    </div>

    <div class="grid">
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
    padding-bottom: 42px;
  }

  .head {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    gap: 24px;
    margin-bottom: 18px;
  }

  .head p {
    margin: 0;
    font-size: 12px;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: var(--brand);
    font-weight: 700;
  }

  .head h2 {
    margin: 0;
    max-width: 760px;
    font-size: 42px;
    letter-spacing: -0.02em;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
  }

  article {
    border-radius: 16px;
    background: #fff;
    border: 1px solid var(--line);
    padding: 22px;
    min-height: 188px;
  }

  h3 {
    margin: 0 0 10px;
    font-size: 22px;
  }

  article p {
    margin: 0;
    color: var(--text-2);
    line-height: 1.5;
  }

  @media (max-width: 1327px) {
    .head {
      display: block;
    }

    .head h2 {
      margin-top: 8px;
      font-size: 34px;
    }

    .grid {
      grid-template-columns: 1fr;
    }
  }
</style>
