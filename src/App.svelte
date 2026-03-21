<script>
  import Nav from './lib/Nav.svelte'
  import Home from './lib/pages/Home.svelte'
  import Experience from './lib/pages/Experience.svelte'
  import Projects from './lib/pages/Projects.svelte'
  import Blog from './lib/pages/Blog.svelte'
  import Me from './lib/pages/Me.svelte'

  let currentPage = 'home'

  function navigate(event) {
    currentPage = event.detail
    window.scrollTo(0, 0)
  }
</script>

<Nav {currentPage} on:navigate={navigate} />

{#if currentPage === 'home'}
  <Home on:navigate={navigate} />
{:else if currentPage === 'experience'}
  <Experience />
{:else if currentPage === 'projects'}
  <Projects />
{:else if currentPage === 'blog'}
  <Blog />
{:else if currentPage === 'me'}
  <Me />
{/if}
