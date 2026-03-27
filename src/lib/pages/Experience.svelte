<script>
  const sections = [
    {
      label: 'Current',
      items: [
        {
          logo: 'MA',
          title: 'AI Systems Research Intern',
          company: 'Mach-AI · Internship',
          desc: 'Working with LLMs, MCP servers, and agentic systems.',
          location: 'Los Angeles, CA',
          date: 'Jan 2026 – Present',
        },
        {
          logo: 'SE',
          title: 'Founding Data Engineer',
          company: 'Stealth Startup',
          desc: 'Maintaining and automating data pipelines for AI systems.',
          location: 'New Brunswick, NJ',
          date: 'Feb 2026 – Present',
        },
        {
          logo: 'MSA',
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
          logo: 'RU',
          title: 'CS112 Course Staff',
          company: 'Rutgers University · Part-time',
          desc: 'Supporting students in CS112 (Data Structures) on Piazza and with course-related queries.',
          location: 'New Brunswick, NJ',
          date: 'Jan 2026 – Present',
        },
        {
          logo: 'RU',
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
          logo: 'BP',
          title: 'Product Marketing Fellow',
          company: 'Blueprint · Fellowship',
          desc: 'Worked on the RU Shopping marketing plan and built a research-backed launch strategy with my team.',
          location: 'New Brunswick, NJ',
          date: 'Oct 2025 – Dec 2025',
        },
        {
          logo: 'ISCJ',
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
          logo: 'BTT',
          title: 'AI/ML Fellow',
          company: 'Break Through Tech · Fellowship',
          desc: 'Selected for the 2026–2027 cohort. Completing ML Foundations and working on industry projects with partner companies.',
          location: 'Remote',
          date: 'Mar 2026 – Present',
        },
        {
          logo: 'A4A',
          title: 'Ignite Fellow',
          company: 'AI4ALL · Program',
          desc: 'Selected for AI4ALL Ignite, a competitive AI education and mentorship program.',
          location: 'Remote',
          date: 'Dec 2025 – Oct 2026',
        },
        {
          logo: 'CP',
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
          <div class="exp-logo">{exp.logo}</div>
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