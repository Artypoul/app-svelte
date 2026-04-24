<svelte:head>
  <title>Особенная мама — главная</title>
  <meta
    name="description"
    content="Главная страница платформы поддержки семей: проверенные фонды, инструкции, истории и маршруты помощи."
  />
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          screens: {
            xs: '390px'
          },
          colors: {
            ink: '#080808',
            text: '#111111',
            muted: '#5C5F63',
            surface: '#F5F4F0',
            line: '#DDDCD6',
            violet: '#7B2CFF',
            olive: '#9DBB60',
            orange: '#EB5B23',
            card: '#EEF2FB'
          },
          boxShadow: {
            soft: '0 24px 60px -18px rgba(0, 0, 0, 0.22)',
            glow: '0 18px 42px -16px rgba(123, 44, 255, 0.34)',
            orange: '0 18px 40px -18px rgba(235, 91, 35, 0.45)'
          },
          borderRadius: {
            '4xl': '32px',
            '5xl': '40px'
          },
          fontFamily: {
            sans: ['Inter', 'ui-sans-serif', 'system-ui', 'sans-serif'],
            display: ['Inter', 'ui-sans-serif', 'system-ui', 'sans-serif'],
            serif: ['"Times New Roman"', 'Georgia', 'serif']
          },
          maxWidth: {
            '8xl': '1440px'
          },
          letterSpacing: {
            tighter2: '-0.04em'
          }
        }
      }
    };
  </script>
</svelte:head>

<div class="min-h-screen bg-grid text-text antialiased">
  <header class="sticky top-0 z-50 border-b border-line/80 bg-surface/80 backdrop-blur-xl">
    <div class="mx-auto flex max-w-8xl items-center justify-between px-4 py-3 xs:px-5 md:px-6 lg:px-8">
      <a href="#hero" class="flex items-center gap-3">
        <span class="flex h-9 w-9 items-center justify-center rounded-full bg-violet/10 text-violet">
          <svg viewBox="0 0 24 24" class="h-5 w-5 fill-current" aria-hidden="true"><path d="M12 21s-6.7-4.35-8.93-9.01C1.4 8.46 3.2 4.5 7.1 4.5c2.02 0 3.45.98 4.4 2.37.95-1.39 2.38-2.37 4.4-2.37 3.9 0 5.7 3.96 4.03 7.49C18.7 16.65 12 21 12 21Z" /></svg>
        </span>
        <span class="text-base font-extrabold tracking-tighter2 xs:text-lg md:text-xl">Особенная мама</span>
      </a>

      <nav class="hidden items-center gap-7 text-sm font-medium text-muted lg:flex">
        <a href="#help" class="transition hover:text-text">Получить помощь</a>
        <a href="#navigator" class="transition hover:text-text">Навигатор фондов</a>
        <a href="#materials" class="transition hover:text-text">Материалы</a>
        <a href="#stories" class="transition hover:text-text">Истории</a>
        <a href="#about" class="transition hover:text-text">О проекте</a>
      </nav>

      <div class="flex items-center gap-2 xs:gap-3 md:gap-4">
        <a href="#donate" class="hidden text-sm font-semibold text-orange transition hover:opacity-80 lg:inline-block">Поддержать</a>
        <a href="#help" class="inline-flex items-center justify-center rounded-full bg-ink px-4 py-2.5 text-xs font-bold text-white shadow-soft transition hover:-translate-y-0.5 xs:text-sm md:px-5">Найти помощь</a>
      </div>
    </div>
  </header>

  <main>
    <section id="hero" class="px-4 pb-10 pt-6 xs:px-5 md:px-6 md:pb-14 md:pt-8 lg:px-8 lg:pb-20 lg:pt-10">
      <div class="mx-auto max-w-8xl">
        <div class="hero-shell overflow-hidden rounded-4xl border border-white/70 shadow-soft">
          <div class="grid gap-8 px-4 py-5 xs:px-5 xs:py-6 md:px-8 md:py-8 lg:grid-cols-[minmax(0,540px)_minmax(0,1fr)] lg:gap-10 lg:px-10 lg:py-10 xl:grid-cols-[minmax(0,600px)_minmax(0,1fr)] xl:px-12 xl:py-12">
            <div class="flex flex-col justify-center">
              <div class="mb-4 inline-flex w-fit items-center gap-2 rounded-full border border-line bg-white px-3 py-1.5">
                <span class="h-2 w-2 rounded-full bg-olive"></span>
                <span class="text-[11px] font-semibold text-muted xs:text-xs">Платформа поддержки семей</span>
              </div>

              <h1 class="max-w-[16ch] font-display text-[34px] font-black leading-[0.98] tracking-tighter2 text-text xs:text-[38px] sm:text-[44px] md:text-[56px] lg:text-[62px] xl:text-[74px]">
                Вы не одни.
                <span class="block text-orange">Маршрут помощи</span>
                для особенных мам.
              </h1>

              <p class="mt-5 max-w-[56ch] text-sm leading-6 text-muted xs:text-[15px] md:text-base md:leading-7 xl:text-[18px] xl:leading-8">
                Единая база проверенных фондов, понятные инструкции к действию и опыт тех, кто уже прошел этот путь.
              </p>

              <div class="mt-6 flex flex-wrap gap-3 md:mt-7 lg:mt-8">
                <a href="#help" class="inline-flex items-center gap-2 rounded-full bg-violet px-5 py-3 text-sm font-bold text-white shadow-glow transition hover:-translate-y-0.5 md:px-6 md:py-3.5">
                  <span>Получить помощь</span>
                  <span aria-hidden="true">›</span>
                </a>
                <a href="#navigator" class="inline-flex items-center rounded-full border border-line bg-white px-5 py-3 text-sm font-bold text-text transition hover:border-violet/35 hover:bg-white md:px-6 md:py-3.5">Найти фонд</a>
                <a href="#donate" class="inline-flex items-center rounded-full border border-transparent px-3 py-3 text-sm font-semibold text-muted underline underline-offset-4 transition hover:text-text">Поддержать проект</a>
              </div>

              <div class="mt-7 grid gap-2 border-t border-line pt-4 text-xs font-medium text-muted xs:grid-cols-2 md:grid-cols-3 md:gap-3 md:text-sm">
                <div class="flex items-center gap-2"><span class="text-olive">•</span><span>Проверенные фонды</span></div>
                <div class="flex items-center gap-2"><span class="text-orange">•</span><span>Понятные шаги</span></div>
                <div class="flex items-center gap-2"><span class="text-violet">•</span><span>Поддержка равных</span></div>
              </div>
            </div>

            <div class="relative flex items-center justify-center lg:justify-end">
              <div class="hero-image-mask w-full overflow-hidden rounded-[28px] bg-white shadow-soft md:rounded-[32px] lg:max-w-[760px] xl:max-w-[820px]">
                <img src="https://www.figma.com/api/mcp/asset/8bbb9320-bc8b-4dba-a97e-06d11e149688" alt="Мама с ребёнком" class="h-[280px] w-full object-cover object-[34%_center] xs:h-[320px] md:h-[420px] lg:h-[560px] xl:h-[640px]" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="help" class="px-4 py-8 xs:px-5 md:px-6 md:py-10 lg:px-8 lg:py-14">
      <div class="mx-auto max-w-8xl">
        <div class="rounded-4xl border border-white/70 bg-white/72 px-4 py-5 shadow-soft backdrop-blur-sm xs:px-5 md:px-8 md:py-8">
          <div class="mb-6 md:mb-8 lg:mb-10">
            <h2 class="font-display text-[28px] font-black leading-[1.02] tracking-tighter2 md:text-[36px] lg:text-[42px]">Выберите ваш путь</h2>
            <p class="mt-3 max-w-[60ch] text-sm leading-6 text-muted md:text-base">Мы структурировали информацию, чтобы вы могли быстро найти именно то, что нужно сейчас.</p>
          </div>
          <div class="grid gap-3 md:grid-cols-2 lg:grid-cols-4 lg:gap-4">
            <article class="rounded-4xl bg-surface p-5 md:p-6 lg:p-7"><h3 class="text-lg font-bold leading-6">Мне нужна помощь</h3><p class="mt-8 text-sm leading-6 text-muted">С чего начать после диагноза, как получить квоту или найти психолога.</p></article>
            <article class="rounded-4xl bg-surface p-5 md:p-6 lg:p-7"><h3 class="text-lg font-bold leading-6">Хочу найти фонд</h3><p class="mt-8 text-sm leading-6 text-muted">Единая база проверенных НКО по регионам и диагнозам.</p></article>
            <article class="rounded-4xl bg-surface p-5 md:p-6 lg:p-7"><h3 class="text-lg font-bold leading-6">Хочу разобраться</h3><p class="mt-8 text-sm leading-6 text-muted">Инструкции по реабилитации, юридическим правам и школе.</p></article>
            <article class="rounded-4xl bg-surface p-5 md:p-6 lg:p-7"><h3 class="text-lg font-bold leading-6">Хочу помочь</h3><p class="mt-8 text-sm leading-6 text-muted">Сделать пожертвование, стать волонтёром или партнёром проекта.</p></article>
          </div>
        </div>
      </div>
    </section>

    <section id="navigator" class="px-4 py-4 xs:px-5 md:px-6 md:py-6 lg:px-8 lg:py-8">
      <div class="section-dark mx-auto max-w-8xl overflow-hidden rounded-5xl px-4 py-8 text-white shadow-soft xs:px-5 md:px-8 md:py-10 lg:px-10 lg:py-12 xl:px-12 xl:py-16">
        <h2 class="mt-4 font-display text-[28px] font-black leading-[1.02] tracking-tighter2 md:text-[38px] lg:text-[46px]">Навигатор по фондам</h2>
      </div>
    </section>

    <section id="materials" class="px-4 py-10 xs:px-5 md:px-6 md:py-12 lg:px-8 lg:py-16">
      <div class="mx-auto max-w-8xl">
        <h2 class="font-display text-[28px] font-black leading-[1.02] tracking-tighter2 md:text-[36px] lg:text-[42px]">Полезные материалы</h2>
      </div>
    </section>

    <section id="donate" class="px-4 py-10 xs:px-5 md:px-6 md:py-12 lg:px-8 lg:py-16">
      <div class="section-orange mx-auto max-w-8xl rounded-5xl px-4 py-8 text-white shadow-orange xs:px-5 md:px-8 md:py-10 lg:px-10 lg:py-14 xl:px-12">
        <h2 class="font-display text-[28px] font-black leading-[1.02] tracking-tighter2 md:text-[38px] lg:text-[46px]">Поддержите проект</h2>
      </div>
    </section>
  </main>
</div>
