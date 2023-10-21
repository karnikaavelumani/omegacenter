<script lang="ts">
  import App from '$lib/components/App.svelte';
</script>

<div>
  <App />
</div>

<style>
  :global(body) {
    margin: 0;
  }

  div {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50vw;
    height: 50vh;
  }
</style>
