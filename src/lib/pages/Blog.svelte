<script>
  const posts = [
    {
      year: '2025',
      items: [
        {
          title: 'Graph-Based Fraud Detection: What I Learned Building with GraphSAGE',
          href: '#',
          desc: 'A writeup of the IBM Datathon project — why graph neural networks make sense for fraud, what GraphSAGE actually does, and what I\'d do differently with more time.',
          date: 'Mar 2025',
          tags: ['ML'],
        },
        {
          title: 'Building a Fall Detection System in 24 Hours',
          href: '#',
          desc: 'How my team went from zero to a working YOLOv8-based fall detection system at a neuroscience + AI hackathon. Dataset issues, time pressure, and what we shipped.',
          date: 'Feb 2025',
          tags: ['CV', 'Hackathon'],
        },
        {
          title: 'Placeholder Article Title — Something You Actually Want to Write',
          href: '#',
          desc: 'Placeholder description. One or two sentences about what the article covers. Keep it honest, not marketing-y.',
          date: 'Jan 2025',
          tags: ['Opinion'],
        },
      ],
    },
    {
      year: '2024',
      items: [
        {
          title: 'Another Placeholder — Earlier Writing',
          href: '#',
          desc: 'Placeholder. Even if older writing is rougher, keeping it shows growth. Don\'t hide it.',
          date: 'Dec 2024',
          tags: ['Misc'],
        },
      ],
    },
  ]

  let openItems = new Set()

  function toggleItem(id) {
    if (openItems.has(id)) {
      openItems.delete(id)
    } else {
      openItems.add(id)
    }
    openItems = openItems
  }
</script>

<div class="page">
  <h1 class="page-title">Writing.</h1>

  <div class="blog-list">
    {#each posts as group, gi}
      <div class="blog-year" class:first={gi === 0}>{group.year}</div>
      {#each group.items as post, pi}
        {@const id = `${gi}-${pi}`}
        <div class="blog-item">
          <div class="blog-item-top">
            <a class="blog-title" href={post.href} target="_blank">{post.title}</a>
            <button
              class="blog-toggle"
              class:open={openItems.has(id)}
              aria-label="Show description"
              on:click={() => toggleItem(id)}
            >
              {openItems.has(id) ? '−' : '+'}
            </button>
          </div>
          {#if openItems.has(id)}
            <div class="blog-desc">{post.desc}</div>
          {/if}
          <div class="blog-meta">
            <span class="blog-date">{post.date}</span>
            {#each post.tags as tag}
              <span class="blog-tag-pill">{tag}</span>
            {/each}
          </div>
        </div>
      {/each}
    {/each}
  </div>
</div>

<style>
  .blog-year.first {
    border-top: none;
    padding-top: 0;
    margin-top: 0;
  }
</style>
