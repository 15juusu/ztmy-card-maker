<script lang="ts">
  let {
    element
  }: {
    element: 'darkness' | 'electric' | 'flame' | 'wind';
  } = $props();

  let getBgUrl = (): string => {
    return `/images/bg-card-element-${element}.jpg`;
  };
</script>

<div class="container" style:background-image={`url(${getBgUrl()})`}></div>

<style>
  .container {
    aspect-ratio: 700 / 977;
    background-color: white;
    background-position: center;
    background-size: cover;
    height: auto;
    max-height: 100%;
    max-width: 512px;
    width: 100%;
  }
</style>
