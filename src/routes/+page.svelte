<script>
  import Greet from '../lib/Greet.svelte'
</script>

<div class="justify-center text-center border-gray-950 m-4">
  <h1 class="text-3xl font-bold p-4">Welcome to SvelteKit</h1>
  <Greet />
</div>

<style lang="postcss">
  :global(html) {
    color: theme(colors.white);
    background-color: theme(colors.gray.700);
  }
</style>
