<script>
  import { invoke } from '@tauri-apps/api/tauri'

  let name = ''
  let greetMsg = ''

  async function greet() {
    greetMsg = await invoke('greet', { name })
  }
</script>

<div class="justify-center m-4 text-center grid place-items-center">
  <input
    class="bg-slate-800 h-9 p-1 m-1 border-2 border-slate-600 rounded-lg"
    id="greet-input"
    placeholder="Enter a name..."
    bind:value={name}
  />
  <button class="bg-green-500 p-1 m-1 border-2 border-green-600 rounded-lg" on:click={greet}
    >Greet</button
  >
  {#if greetMsg}
    <p class="bg-blue-500 w-10/12 p-1 m-1 border-2 border-blue-600 rounded-lg">{greetMsg}</p>
  {/if}
</div>
