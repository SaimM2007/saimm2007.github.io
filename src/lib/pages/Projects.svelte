<script>
  const featured = [
    {
      name: 'FraudNet',
      desc: 'Graph-based fraud detection using GraphSAGE on financial transaction networks. Trained on IBM AMLSim dataset, deployed via FastAPI.',
      links: [{ text: 'github ↗', href: '#' }, { text: 'demo ↗', href: '#' }],
      tags: [{ label: 'ML' }, { label: 'Python', cls: 'lang' }, { label: 'PyTorch', cls: 'lang' }],
    },
    {
      name: 'FallGuard',
      desc: 'Real-time fall detection system using YOLOv8n + OpenCV. Built for neurological motor impairment monitoring. Alerts via Twilio SMS.',
      links: [{ text: 'github ↗', href: '#' }],
      tags: [{ label: 'ML' }, { label: 'CV' }, { label: 'Python', cls: 'lang' }],
    },
    {
      name: 'PulseFeed',
      desc: 'AI-powered news aggregator that clusters articles by topic using sentence transformers and serves a personalized feed via a lightweight web UI.',
      links: [{ text: 'github ↗', href: '#' }, { text: 'live ↗', href: '#' }],
      tags: [{ label: 'NLP' }, { label: 'Python', cls: 'lang' }, { label: 'JS', cls: 'lang' }],
    },
    {
      name: 'NeuralLearn',
      desc: 'Adaptive learning platform that adjusts difficulty based on student performance. Built with a custom spaced repetition algorithm and a React frontend.',
      links: [{ text: 'github ↗', href: '#' }],
      tags: [{ label: 'Web' }, { label: 'JS', cls: 'lang' }, { label: 'Python', cls: 'lang' }],
    },
  ]

  const allProjects = [
    {
      name: 'FraudNet',
      desc: 'Graph-based fraud detection with GraphSAGE on financial transaction networks.',
      filterTags: 'ML Python College Hackathon',
      searchName: 'fraudnet fraud graph detection',
      tags: [{ label: 'ML' }, { label: 'Python', cls: 'lang' }, { label: 'PyTorch', cls: 'lang' }, { label: 'College', cls: 'era' }, { label: 'Hackathon', cls: 'hackathon' }],
      links: [{ text: 'gh ↗', href: '#' }],
    },
    {
      name: 'FallGuard',
      desc: 'Real-time fall detection for neurological motor impairment monitoring using YOLOv8.',
      filterTags: 'ML CV Python College Hackathon',
      searchName: 'fallguard fall detection yolo',
      tags: [{ label: 'ML' }, { label: 'CV' }, { label: 'Python', cls: 'lang' }, { label: 'College', cls: 'era' }, { label: 'Hackathon', cls: 'hackathon' }],
      links: [{ text: 'gh ↗', href: '#' }],
    },
    {
      name: 'PulseFeed',
      desc: 'AI news aggregator with topic clustering via sentence transformers.',
      filterTags: 'Web JS Python College',
      searchName: 'pulsefeed news aggregator nlp',
      tags: [{ label: 'NLP' }, { label: 'Python', cls: 'lang' }, { label: 'JS', cls: 'lang' }, { label: 'College', cls: 'era' }],
      links: [{ text: 'gh ↗', href: '#' }, { text: 'live ↗', href: '#' }],
    },
    {
      name: 'NeuralLearn',
      desc: 'Adaptive learning platform with custom spaced repetition algorithm.',
      filterTags: 'Web JS Python College',
      searchName: 'neurallearn adaptive learning platform',
      tags: [{ label: 'Web' }, { label: 'JS', cls: 'lang' }, { label: 'Python', cls: 'lang' }, { label: 'College', cls: 'era' }],
      links: [{ text: 'gh ↗', href: '#' }],
    },
    {
      name: 'AutoPipe',
      desc: 'CLI tool for automating data preprocessing pipelines. Config-driven, supports 6 file formats.',
      filterTags: 'Tool Python College',
      searchName: 'script automation cli tool',
      tags: [{ label: 'Tool' }, { label: 'Python', cls: 'lang' }, { label: 'College', cls: 'era' }],
      links: [{ text: 'gh ↗', href: '#' }],
    },
    {
      name: 'GridLock',
      desc: 'Browser-based puzzle game with procedurally generated levels. Made in a weekend for fun.',
      filterTags: 'Game JS College',
      searchName: 'game browser puzzle fun',
      tags: [{ label: 'Game' }, { label: 'JS', cls: 'lang' }, { label: 'College', cls: 'era' }],
      links: [{ text: 'gh ↗', href: '#' }, { text: 'play ↗', href: '#' }],
    },
    {
      name: 'malloc-lite',
      desc: 'Custom memory allocator in C. Implements first-fit, best-fit, and buddy system strategies.',
      filterTags: 'Systems C College',
      searchName: 'systems low level c memory allocator',
      tags: [{ label: 'Systems' }, { label: 'C', cls: 'lang' }, { label: 'College', cls: 'era' }],
      links: [{ text: 'gh ↗', href: '#' }],
    },
    {
      name: 'SpamZapper',
      desc: 'My first real ML project. Naive Bayes spam classifier trained on the Enron dataset. Where it all started.',
      filterTags: 'ML Python HS',
      searchName: 'first ml project classifier hs',
      tags: [{ label: 'ML' }, { label: 'Python', cls: 'lang' }, { label: 'HS', cls: 'era' }],
      links: [{ text: 'gh ↗', href: '#' }],
    },
    {
      name: 'Asteroid Run',
      desc: 'Pygame arcade shooter. First time I stayed up until 3am because I couldn\'t stop adding features.',
      filterTags: 'Game Python HS',
      searchName: 'pygame game hs fun',
      tags: [{ label: 'Game' }, { label: 'Python', cls: 'lang' }, { label: 'HS', cls: 'era' }],
      links: [{ text: 'gh ↗', href: '#' }],
    },
  ]

  const filterOptions = [
    { label: 'ML', cls: 'type' },
    { label: 'Web', cls: 'type' },
    { label: 'Game', cls: 'type' },
    { label: 'Tool', cls: 'type' },
    { label: 'Systems', cls: 'type' },
    { label: 'CV', cls: 'type' },
    { label: 'Python', cls: 'lang' },
    { label: 'C', cls: 'lang' },
    { label: 'JS', cls: 'lang' },
    { label: 'HS', cls: 'era' },
    { label: 'College', cls: 'era' },
    { label: 'Hackathon', cls: 'hackathon' },
  ]

  const INITIAL_SHOW = 6

  let activeFilters = new Set()
  let searchQuery = ''
  let showAll = false

  $: filteredProjects = allProjects.filter(p => {
    const q = searchQuery.toLowerCase()
    const matchesSearch = !q || p.searchName.includes(q) || p.filterTags.toLowerCase().includes(q)
    const matchesFilter = activeFilters.size === 0 || [...activeFilters].every(f => p.filterTags.includes(f))
    return matchesSearch && matchesFilter
  })

  $: displayedProjects = showAll ? filteredProjects : filteredProjects.slice(0, INITIAL_SHOW)
  $: showMoreVisible = filteredProjects.length > INITIAL_SHOW && !showAll

  function toggleFilter(label) {
    if (activeFilters.has(label)) {
      activeFilters.delete(label)
    } else {
      activeFilters.add(label)
    }
    activeFilters = activeFilters
    showAll = false
  }
</script>

<div class="page">
  <h1 class="page-title">Projects</h1>

  <p class="section-label">Featured</p>
  <div class="projects-featured">
    {#each featured as proj}
      <div class="proj-card-featured">
        <div class="proj-name">{proj.name}</div>
        <div class="proj-desc">{proj.desc}</div>
        <div class="proj-links">
          {#each proj.links as link}
            <a class="proj-link" href={link.href}>{link.text}</a>
          {/each}
        </div>
        <div class="tags">
          {#each proj.tags as tag}
            <span class="tag {tag.cls || ''}">{tag.label}</span>
          {/each}
        </div>
      </div>
    {/each}
  </div>

  <p class="section-label" style="margin-top: 2.5rem;">All Projects</p>

  <div class="search-wrap">
    <span class="search-icon">⌕</span>
    <input
      class="search-input"
      type="text"
      placeholder="Search projects..."
      bind:value={searchQuery}
      on:input={() => { showAll = false }}
    />
  </div>

  <div class="filter-bar">
    <span class="filter-label">Filter</span>
    {#each filterOptions as opt}
      <span
        class="tag {opt.cls} filter-tag"
        class:active={activeFilters.has(opt.label)}
        on:click={() => toggleFilter(opt.label)}
        role="button"
        tabindex="0"
        on:keydown={e => e.key === 'Enter' && toggleFilter(opt.label)}
      >
        {opt.label}
      </span>
    {/each}
  </div>

  <div class="proj-list">
    {#each displayedProjects as proj}
      <div class="proj-list-item">
        <div class="proj-list-main">
          <div class="proj-list-name">{proj.name}</div>
          <div class="proj-list-desc">{proj.desc}</div>
          <div class="proj-list-tags">
            {#each proj.tags as tag}
              <span class="tag {tag.cls || ''}">{tag.label}</span>
            {/each}
          </div>
        </div>
        <div class="proj-list-links">
          {#each proj.links as link}
            <a class="proj-link" href={link.href}>{link.text}</a>
          {/each}
        </div>
      </div>
    {/each}
  </div>

  {#if showMoreVisible}
    <button class="show-more-btn" on:click={() => { showAll = true }}>
      Show more projects
    </button>
  {/if}
</div>