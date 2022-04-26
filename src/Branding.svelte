<script>
  import {theme$} from './store';

  let themeVal;

  theme$.subscribe((theme) => {
    themeVal = theme;
  });

</script>

<article class="branding">
  <p>Bloomberg</p>
</article>


<style>
  .branding {
    height: 8rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .branding p {
    font-size: 3rem;
  }

</style>