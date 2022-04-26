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
    height: 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .branding p {
    font-size: 3rem;
    margin: 0 !important
  }

</style>