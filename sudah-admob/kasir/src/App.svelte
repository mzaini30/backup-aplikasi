<script>
  import Router from "svelte-spa-router";
  // @ts-ignore
  import routes from "virtual:generated-pages-svelte";
  import "@unocss/reset/tailwind.css";
  // import "warna-tailwind/warna.css";
  import "./App.css";
  // import "uno.css";
  import stat_aja from "stat-aja";

  // stat_aja({ judul: "Judul Aplikasi", tipe: "Aplikasi Android" });
</script>

<div class="p-3 grid grid-cols-6 gap-2">
  <div class="col-span-6 sm:col-span-1">
    <ul class="menu bg-base-200 mb-3 w-full rounded-box">
      <li><a href="#/">Beranda</a></li>
      <li><a href="#/list-harga">List Harga</a></li>
      <li><a href="#/rekap">Rekap</a></li>
    </ul>
    <ul class="menu bg-base-200 w-full rounded-box">
      <li>
        <a
          href="https://play.google.com/store/apps/details?id=com.mzaini30.kasir"
          >Review App</a
        >
      </li>
      <li>
        <a href="https://play.google.com/store/apps/dev?id=5401138465689796048"
          >Other Apps</a
        >
      </li>
    </ul>
  </div>
  <div class="col-span-6 sm:col-span-5">
    <Router {routes} />
  </div>
</div>
