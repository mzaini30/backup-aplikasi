<script>
  import Router from "svelte-spa-router";
  import routes from "virtual:generated-pages-svelte";
  import Header from "header-apk";
</script>

  <Router {routes} />

<style>
  :global(*) {
    word-wrap: break-word;
  }
  /* chrome extension */
  /* :global(body) {
    width: 350px;
    height: 500px;
    font-size: 16px;
  } */
</style>
