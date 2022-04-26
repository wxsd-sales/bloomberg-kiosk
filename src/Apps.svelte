<script>
  import Carousel from 'svelte-carousel';
  import Lirr from './Lirr.svelte';

  let carousel;

  const handleNextClick = () => {
    carousel.goToNext();
  };
</script>

<article class="apps">
  <svelte:component
    this={Carousel}
    bind:this={carousel}
    >
      <Lirr />
      <h3>App 2</h3>
      <h3>App 3</h3>
  </svelte:component>
</article>


<style>
  .apps {
    height: 30rem;
  }
</style>