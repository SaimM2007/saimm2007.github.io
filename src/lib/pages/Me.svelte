<script>
  const sections = [
    {
      title: 'gaming',
      content: 'Placeholder — write about what games you actually play, why you got into it, maybe how it connects to your interest in computers or systems. This is where you get to actually talk about yourself. Don\'t be concise here, that\'s the whole point of this page.',
    },
    {
      title: 'teaching',
      content: 'I TA data structures at Rutgers and it\'s one of the things I genuinely look forward to. There\'s something about having to explain a concept clearly enough that someone else gets it — it forces you to actually understand it yourself. Office hours, recitations, debugging someone\'s linked list at 11pm — I\'m into it. I\'ve also done tutoring outside of school, and I think I want to keep finding ways to teach whatever I\'m learning.',
    },
    {
      title: 'hackathons',
      content: 'The 24-48 hour format genuinely appeals to me. You pick a problem, you build something real, and you ship it whether or not it\'s perfect. I\'ve done the Rutgers BITS x IBM Datathon where we built a graph-based fraud detection network, and a neuroscience + AI hackathon where we built a real-time fall detection system using YOLOv8. There will be more. The crunch is the fun part.',
    },
    {
      title: 'building random stuff',
      content: 'Placeholder — talk about the random projects you make for fun with no audience in mind. The ones that never go on a resume. The ones you made at 2am because you thought it\'d be funny or cool or useful to you specifically. This section is where those live.',
    },
    {
      title: 'placeholder hobby',
      content: 'Add something genuinely personal here — something that has nothing to do with CS. A sport, a creative thing, something you\'ve been doing since you were a kid. This is the most memorable section of the page, don\'t skip it.',
    },
  ]
</script>

<div class="page">
  <h1 class="page-title">Me.</h1>

  <div class="me-sections">
    {#each sections as section}
      <div class="me-section">
        <h2 class="me-section-title">{section.title}</h2>
        <p>{section.content}</p>
      </div>
    {/each}

    <div class="me-section me-thanks">
      <h2 class="me-section-title">thanks for reading.</h2>
      <p>
        If you made it this far you probably get the vibe. Feel free to reach out —
        <a class="me-link" href="#">email</a>,
        <a class="me-link" href="#">LinkedIn</a>,
        or wherever.
      </p>
    </div>
  </div>
</div>
