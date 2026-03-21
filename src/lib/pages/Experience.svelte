<script>
  const sections = [
    {
      label: 'Current',
      items: [
        {
          logo: 'AC',
          title: 'Software Engineer Intern',
          company: 'Acme Corp · Internship',
          desc: 'Building ML-powered features for real-time data pipelines. Working across the full stack with a focus on model integration and backend systems.',
          location: 'New York, NY',
          date: 'Summer 2025',
        },
        {
          logo: 'ML',
          title: 'Machine Learning Researcher',
          company: 'Some Lab · Research',
          desc: 'Investigating graph neural networks for fraud detection. Implemented GraphSAGE-based pipeline on financial datasets with 94% recall.',
          location: 'Remote',
          date: 'Spring 2025',
        },
      ],
    },
    {
      label: 'Teaching & Leadership',
      items: [
        {
          logo: 'TA',
          title: 'Teaching Assistant — Data Structures',
          company: 'Rutgers University · Part-time',
          desc: 'Running weekly office hours and recitations for ~120 students. Grading assignments, writing test cases, and helping students debug their first real algorithms.',
          location: 'New Brunswick, NJ',
          date: '2024 – Present',
        },
        {
          logo: 'HK',
          title: 'Hackathon Organizer',
          company: 'Rutgers Tech Community · Leadership',
          desc: 'Coordinating logistics, sponsorships, and workshops for a 200+ person hackathon. Built internal tooling to manage registrations and team matching.',
          location: 'New Brunswick, NJ',
          date: '2024 – Present',
        },
      ],
    },
    {
      label: 'Earlier',
      items: [
        {
          logo: 'OT',
          title: 'ML Engineer',
          company: 'Outamation · Contract',
          desc: 'Built agentic automation pipelines using LLMs. Shipped a document processing system that reduced manual review time by ~60%.',
          location: 'Remote',
          date: '2023',
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
