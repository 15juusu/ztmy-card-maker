<script lang="ts">
  import { onMount } from 'svelte';

  let {
    element
  }: {
    element: 'darkness' | 'electric' | 'flame' | 'wind';
  } = $props();

  let container: HTMLDivElement;
  let scaleUnit: number = $state(0);

  let setScaleUnit = () => {
    scaleUnit = container.offsetWidth * 0.05;
  };

  let getBgUrl = (): string => {
    return `/images/bg-card-element-${element}.jpg`;
  };

  onMount(() => {
    setScaleUnit();
    window.addEventListener('resize', setScaleUnit);

    return () => {
      window.removeEventListener('resize', setScaleUnit);
    };
  });
</script>

<div
  class="container"
  style:background-image={`url(${getBgUrl()})`}
  style:border-radius={`${scaleUnit}px`}
  bind:this={container}
></div>

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
