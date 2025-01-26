<script lang="ts">
  import Card from '$editor/components/Card.svelte';
</script>

<div class="container">
  <div class="column">
    <Card element="wind" />
  </div>
  <div class="column">
    <h1>ZUTOMAYO</h1>
  </div>
</div>

<style>
  :global(body) {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
  }

  .container {
    background-color: #e6e9f1;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    height: 100dvh;
  }

  .column {
    align-items: center;
    box-sizing: border-box;
    display: flex;
    flex: 1;
    justify-content: center;
    padding: 2rem;
  }

  @media (min-width: 768px) {
    .container {
      flex-direction: row;
    }
  }
</style>
