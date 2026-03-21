<script>
  import { createEventDispatcher } from 'svelte'
  const dispatch = createEventDispatcher()

  const nowCards = [
    { label: 'Building', val: 'This website. A few projects I\'ll talk about when they\'re ready.' },
    { label: 'Learning', val: 'Linear algebra, systems architecture, and how to write cleaner code under pressure.' },
    { label: 'Reading', val: 'Placeholder book title. Something technical, something not.' },
    { label: 'Thinking about', val: 'How agentic systems will change what "software engineering" even means.' },
  ]

  const facts = [
    '📍 New Brunswick, NJ',
    '🎓 Rutgers CS + Data Science',
    '🧠 ML & Systems',
    '🏆 Hackathon regular',
    '🖥️ RTX 4060 daily driver',
    '✍️ Occasional blogger',
  ]
</script>

<div class="page">
  <div class="home-hero">
    <div class="home-greeting">hey, i'm</div>
    <h1 class="home-name">Saim<br /><em>Placeholder.</em></h1>
    <p class="home-tagline">CS + Data Science @ Rutgers. I build things that think, move, and occasionally catch people falling.</p>

    <div class="home-links">
      <a class="home-link-btn" href="#">Resume ↗</a>
      <a class="home-link-btn ghost" href="#">GitHub</a>
      <a class="home-link-btn ghost" href="#">LinkedIn</a>
      <a class="home-link-btn ghost" href="#">Email</a>
    </div>
  </div>

  <div class="home-section">
    <p class="section-label">About</p>
    <div class="home-bio">
      <p>I started with a Python script that barely ran. Now I care about building systems that actually work — ML pipelines, graph networks, real-time CV — the kind of stuff where the problem is harder than the tutorial.</p>
      <p>Currently a first-year at Rutgers doing CS and Data Science (BAIT). I TA data structures, go deep on hackathons, and try to ship something every few weeks whether or not it's polished.</p>
      <p>I'm into the intersection of ML and systems — when models have to run fast in the real world, not just in a notebook. Also into building for fun, not just for the resume.</p>
    </div>
  </div>

  <div class="home-section">
    <p class="section-label">Currently</p>
    <div class="home-now-grid">
      {#each nowCards as card}
        <div class="home-now-card">
          <div class="home-now-label">{card.label}</div>
          <div class="home-now-val">{card.val}</div>
        </div>
      {/each}
    </div>
  </div>

  <div class="home-section">
    <p class="section-label">Quick facts</p>
    <div class="home-facts">
      {#each facts as fact}
        <span class="fact-pill">{fact}</span>
      {/each}
    </div>
  </div>
</div>
