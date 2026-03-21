<script>
  const nowCards = [
    { label: 'Building', val: 'This website. A few projects I\'ll talk about when they\'re ready.' },
    { label: 'Learning', val: 'Linear algebra, systems architecture, and how to write cleaner code under pressure.' },
    { label: 'Reading', val: 'Placeholder book title. Something technical, something not.' },
    { label: 'Thinking about', val: 'How agentic systems will change what "software engineering" even means.' },
  ]

  const facts = [
    'New Brunswick, NJ',
    'Rutgers CS + Data Science',
    'ML & Systems',
    'Hackathon regular',
    'RTX 4060 daily driver',
    'Occasional blogger',
  ]
</script>

<div class="page">
  <div class="home-hero">
    <div class="home-greeting">hey, i'm</div>
    <h1 class="home-name">Saim<br /><em>building.</em></h1>
    <p class="home-tagline">CS + Data Science @ Rutgers. I build things that think, move, and occasionally catch people falling.</p>

    <div class="home-links">
      <a class="home-link-btn" href="/resume.pdf" target="_blank">Resume ↗</a>

      <!-- GitHub -->
      <a class="home-icon-btn" href="https://github.com/SaimM2007" target="_blank" aria-label="GitHub">
        <svg viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
          <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
        </svg>
      </a>

      <!-- LinkedIn -->
      <a class="home-icon-btn" href="https://linkedin.com/in/YOUR-LINKEDIN" target="_blank" aria-label="LinkedIn">
        <svg viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
          <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
        </svg>
      </a>

      <!-- Email -->
      <a class="home-icon-btn" href="mailto:saimmeher007@gmail.com" aria-label="Email">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg">
          <rect x="2" y="4" width="20" height="16" rx="2"/>
          <path d="m2 7 10 7 10-7"/>
        </svg>
      </a>
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

<style>
  .home-icon-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    border-radius: 8px;
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.08);
    color: var(--text-dim);
    transition: color 0.15s, background 0.15s, border-color 0.15s;
  }
  .home-icon-btn:hover {
    color: var(--text);
    background: rgba(255,255,255,0.09);
    border-color: rgba(255,255,255,0.15);
  }
  .home-icon-btn svg {
    width: 18px;
    height: 18px;
  }
</style>