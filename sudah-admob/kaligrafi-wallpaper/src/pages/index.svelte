<script>
  import data from "../Download Gambar Pinterest.json";
  import { acak } from "kumpulan-tools";

  let terpilih = {};
  let kesempatan = 21;

  function diacak() {
    kesempatan -= 1;

    terpilih = acak(data)[0];
    console.log(terpilih.lokasi_file);
    if (kesempatan < 0) {
      kesempatan = 20;
      Andro.reward();
    }
  }
  diacak();
</script>

<div class="h-screen overflow-hidden flex items-center">
  <img class="w-full" src={terpilih.lokasi_file} alt="" />
</div>
<div class="w-full p-3 fixed bottom-0 gap-3 left-0 flex">
  <button class="btn" onclick="my_modal_1.showModal()">🟰</button>
  <button
    class="btn shrink grow"
    on:click={() => Andro.set_wallpaper(terpilih.lokasi_file)}
    >Set as Wallpaper</button
  >
  <div class="indicator">
    <span class="indicator-item badge badge-primary"
      >{kesempatan == 0 ? "Ad" : kesempatan}</span
    >
    <button class="btn text-3xl btn-secondary" on:click={diacak}>🎲</button>
  </div>
</div>
<dialog id="my_modal_1" class="modal">
  <div class="modal-box">
    <ul class="menu bg-base-200 w-full rounded-box">
      <li><a href={terpilih.link}>Source</a></li>
    </ul>
  </div>
  <form method="dialog" class="modal-backdrop">
    <button>close</button>
  </form>
</dialog>
