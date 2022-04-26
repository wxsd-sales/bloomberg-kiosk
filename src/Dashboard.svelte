<script>
  import {onMount} from 'svelte';
  import Carousel from 'svelte-carousel';

	let carousel;

  const handleNextClick = () => {
		carousel.goToNext();
	};
</script>

<article class="dashboard">
  <svelte:component
    this={Carousel}
    bind:this={carousel}
    >
      <h3>Dashboard 1</h3>
      <h3>Dashboard 2</h3>
      <h3>Dashboard 3</h3>
  </svelte:component>
</article>


<style>
  .dashboard {
    height: 8rem;
  }
</style>