<script>
  const sections = [
    {
      label: 'Current',
      items: [
        {
          logo: '/mach-ai.png',
          title: 'AI Systems Research Intern',
          company: 'Mach-AI · Internship',
          desc: 'Working with LLMs, MCP servers, and agentic systems.',
          location: 'Los Angeles, CA',
          date: 'Jan 2026 – Present',
        },
        {
          logo: null,
          title: 'Founding Data Engineer',
          company: 'Stealth Startup',
          desc: 'Maintaining and automating data pipelines for AI systems.',
          location: 'New Brunswick, NJ',
          date: 'Feb 2026 – Present',
        },
        {
          logo: '/msa.png',
          title: 'Software Engineer Extern',
          company: 'Rutgers MSA · Externship',
          desc: 'Contributing to a project-based initiative through the Rutgers MSA Ladders Externship Program.',
          location: 'New Brunswick, NJ',
          date: 'Mar 2026 – Present',
        },
      ],
    },
    {
      label: 'Teaching & Leadership',
      items: [
        {
          logo: '/rucs.png',
          title: 'CS112 Course Staff',
          company: 'Rutgers University · Part-time',
          desc: 'Supporting students in CS112 (Data Structures) on Piazza and with course-related queries.',
          location: 'New Brunswick, NJ',
          date: 'Jan 2026 – Present',
        },
        {
          logo: '/rucs.png',
          title: 'Founding President',
          company: '[Club Name] · Rutgers University',
          desc: 'Co-founding and leading a new student organization at Rutgers.',
          location: 'New Brunswick, NJ',
          date: '2026 – Present',
        },
      ],
    },
    {
      label: 'Earlier',
      items: [
        {
          logo: '/blueprint.png',
          title: 'Product Marketing Fellow',
          company: 'Blueprint · Fellowship',
          desc: 'Worked on the RU Shopping marketing plan and built a research-backed launch strategy with my team.',
          location: 'New Brunswick, NJ',
          date: 'Oct 2025 – Dec 2025',
        },
        {
          logo: '/iscj.png',
          title: 'Administrative Intern',
          company: 'Islamic Society of Central Jersey',
          desc: 'Digitized 400+ graveyard deed records and built a search system that made record lookup effortless for staff.',
          location: 'Monmouth Junction, NJ',
          date: 'May 2025 – Jun 2025',
        },
      ],
    },
    {
      label: 'Programs',
      items: [
        {
          logo: '/btt.png',
          title: 'AI/ML Fellow',
          company: 'Break Through Tech · Fellowship',
          desc: 'Selected for the 2026–2027 cohort. Completing ML Foundations and working on industry projects with partner companies.',
          location: 'Remote',
          date: 'Mar 2026 – Present',
        },
        {
          logo: '/ai4all.png',
          title: 'Ignite Fellow',
          company: 'AI4ALL · Program',
          desc: 'Selected for AI4ALL Ignite, a competitive AI education and mentorship program.',
          location: 'Remote',
          date: 'Dec 2025 – Oct 2026',
        },
        {
          logo: '/codepath.png',
          title: 'Applied AI Engineering',
          company: 'CodePath · AI110',
          desc: '10-week program in AI engineering and AI-assisted software development.',
          location: 'Remote',
          date: 'Feb 2026 – May 2026',
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
      <div class="glass-card">
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
      </div>
    {/each}
  {/each}
</div>

<style>
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