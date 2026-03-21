<script>
  import { createEventDispatcher } from 'svelte'

  export let currentPage

  const dispatch = createEventDispatcher()

  const navItems = [
    { text: 'Home', page: 'home' },
    { text: 'Experience', page: 'experience' },
    { text: 'Projects', page: 'projects' },
    { text: 'Blog', page: 'blog' },
    { text: 'Me', page: 'me' },
  ]
</script>

<nav>
  {#each navItems as item}
    <a
      href="#"
      class:active={currentPage === item.page}
      on:click|preventDefault={() => dispatch('navigate', item.page)}
    >
      {item.text}
    </a>
  {/each}
</nav>
