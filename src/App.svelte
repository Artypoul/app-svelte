<script>
  import Header from './components/Header.svelte';
  import Footer from './components/Footer.svelte';
  import Hero from './sections/Hero.svelte';
  import Features from './sections/Features.svelte';
  import Cta from './sections/Cta.svelte';
  import { navItems, metrics, featureCards } from './lib/content';
</script>

<div class="page">
  <Header {navItems} />
  <main>
    <Hero {metrics} />
    <Features cards={featureCards} />
    <Cta />
  </main>
  <Footer />
</div>

<style>
  .page {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  main {
    flex: 1;
  }
</style>
