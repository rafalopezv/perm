<script>
  import { dndzone } from 'svelte-dnd-action';
  import { flip } from 'svelte/animate';
  import { createEventDispatcher } from 'svelte';
  export let items = [];
  export let type; // Unique type for functionality
  export let customClass = ''; // Custom class for independent styling

  const flipDurationMs = 200;
  const dispatch = createEventDispatcher();

  // Emit IDs for tracking if the customClass is "light-style"
  function handleSort(e) {
  items = e.detail.items;

  if (customClass === 'light-style') {
    const idsInOrder = items.map(item => item.id);
    dispatch('trackUpdate', idsInOrder); // Emit the event
  }
}
</script>

<div class="container {customClass}">
  <section 
    use:dndzone={{ items, flipDurationMs, type }}
    on:consider={handleSort}
    on:finalize={handleSort}
  >
    {#each items as item (item.id)}
      <div animate:flip={{ duration: flipDurationMs }}>
        <img src={item.src} alt={item.title} />
      </div>
    {/each}
  </section>
</div>

<style>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 100%;
    padding: 0.5em;
  }

  section {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.5em;
    border: none;
    min-height: 17em;
    width: 40%;
    border-radius: 9px;
    padding: 20px;
  }

  /* Independent styles based on customClass */
  .light-style section {
    background-color: #fff0ad;
  }

  .dark-style section {
    background-color: #f9f9f9;
    color: white;
  }

  img {
    width: 100%;
    height: auto;
    outline: none; 
  }

</style>