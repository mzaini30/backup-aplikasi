<script>
  import Router from "svelte-spa-router";
  // @ts-ignore
  import routes from "virtual:generated-pages-svelte";
  // import "@unocss/reset/tailwind.css";
  // import "warna-tailwind/warna.css";
  import "./App.css";
  // import "uno.css";
  import stat_aja from "stat-aja";
  // import "./style-tailwind.css"

  // stat_aja({ judul: "Kaligrafi", tipe: "Aplikasi Android" });
</script>

<Router {routes} />
