<script>
  const sections = [
    {
      label: 'Current',
      items: [
        {
          logo: 'images/mach-ai.png',
          title: 'AI Systems Research Intern',
          company: 'Mach-AI · Internship',
          desc: 'Working with LLMs, MCP servers, and agentic systems.',
          location: 'Los Angeles, CA',
          date: 'Winter 2026',
          url: 'https://mach-ai.com',
        },
        {
          logo: 'images/stealth.png',
          title: 'Founding Data Engineer',
          company: 'Stealth Startup',
          desc: 'Maintaining and automating data pipelines for AI systems.',
          location: 'New Brunswick, NJ',
          date: 'Feb 2026 – Present',
          url: null,
        },
        {
          logo: 'images/msa.png',
          title: 'Software Engineer Extern',
          company: 'Rutgers Muslim Student Association · Externship',
          desc: 'Contributing to a project-based initiative through the Rutgers MSA Ladders Externship Program.',
          location: 'New Brunswick, NJ',
          date: 'Spring 2026',
          url: 'https://www.rutgersmsa.org/',
        },
      ],
    },
    {
      label: 'Teaching & Leadership',
      items: [
        {
          logo: 'images/rucs.png',
          title: 'CS112 Course Staff',
          company: 'Rutgers University · Part-time',
          desc: 'Supporting students in CS112 (Data Structures) on Piazza and with course-related queries.',
          location: 'New Brunswick, NJ',
          date: 'Spring 2026',
          url: 'https://rutgers.edu',
        },
        {
          logo: 'images/rucs.png',
          title: 'Founding President',
          company: '[Club Name] · Rutgers University',
          desc: 'Co-founding and leading a new student organization at Rutgers.',
          location: 'New Brunswick, NJ',
          date: '2026 – Present',
          url: null,
        },
      ],
    },
    {
      label: 'Earlier',
      items: [
        {
          logo: 'images/blueprint.png',
          title: 'Product Marketing Fellow',
          company: 'Blueprint · Fellowship',
          desc: 'Worked on the RU Shopping marketing plan and built a research-backed launch strategy with my team.',
          location: 'New Brunswick, NJ',
          date: 'Fall 2025',
          url: 'https://www.linkedin.com/company/blueprint-rutgers/',
        },
        {
          logo: 'images/iscj.png',
          title: 'Administrative Intern',
          company: 'Islamic Society of Central Jersey',
          desc: 'Digitized 400+ graveyard deed records and built a search system that made record lookup effortless for staff.',
          location: 'Monmouth Junction, NJ',
          date: 'Summer 2025',
          url: 'https://iscj.org',
        },
      ],
    },
    {
      label: 'Programs',
      items: [
        {
          logo: 'images/btt.png',
          title: 'AI/ML Fellow',
          company: 'Break Through Tech · Fellowship',
          desc: 'Selected for the 2026–2027 cohort. Completing ML Foundations and working on industry projects with partner companies.',
          location: 'Remote',
          date: 'Mar 2026 – Present',
          url: 'https://breakthroughtech.org',
        },
        {
          logo: 'images/ai4all.png',
          title: 'Ignite Fellow',
          company: 'AI4ALL · Program',
          desc: 'Selected for AI4ALL Ignite, a competitive AI education and mentorship program.',
          location: 'Remote',
          date: 'Dec 2025 – Oct 2026',
          url: 'https://ai-4-all.org',
        },
        {
          logo: 'images/codepath.png',
          title: 'Applied AI Engineering',
          company: 'CodePath · AI110',
          desc: '10-week program in AI engineering and AI-assisted software development.',
          location: 'Remote',
          date: 'Feb 2026 – May 2026',
          url: 'https://codepath.org',
        },
      ],
    },
  ]
</script>

<div class="page">
  <h1 class="page-title">Experience</h1>

  {#each sections as section}
    <p class="section-label">{section.label}</p>
    {#each section.items as exp}
      <svelte:element
        this={exp.url ? 'a' : 'div'}
        class="glass-card exp-link"
        href={exp.url ?? undefined}
        target={exp.url ? '_blank' : undefined}
        rel={exp.url ? 'noopener noreferrer' : undefined}
      >
        <div class="exp-card">
          <div class="exp-logo">
            {#if exp.logo}
              <img src={exp.logo} alt={exp.company} />
            {:else}
              <span>SE</span>
            {/if}
          </div>
          <div class="exp-main">
            <div class="exp-title">{exp.title}</div>
            <div class="exp-company">{exp.company}</div>
            <div class="exp-desc">{exp.desc}</div>
          </div>
          <div class="exp-meta">
            <div class="exp-location">{exp.location}</div>
            <div class="exp-date">{exp.date}</div>
          </div>
        </div>
      </svelte:element>
    {/each}
  {/each}
</div>

<style>
  .exp-link {
    display: block;
    text-decoration: none;
    color: inherit;
    cursor: pointer;
  }
  .exp-logo {
    width: 48px;
    height: 48px;
    border-radius: 10px;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.1);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    overflow: hidden;
  }
  .exp-logo img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    border-radius: 9px;
  }
  .exp-logo span {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--text-muted);
  }
</style>