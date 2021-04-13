<div>
  <input bind:value="{title}" name="title" placeholder="ชื่อหลัก" />
  <input bind:value="{prefix}" placeholder="อธิบายเพื่อให้ค้นหาได้ง่ายขึ้น" />
  <input bind:value="{url}" placeholder="ลิ้ง" />
  <input bind:value="{image}" placeholder="pdf/csv/picture" />
</div>
<div class="flexbox">
  <div class="box ">Box</div>
  <div class="box ">Box</div>
  <div class="box ">Box</div>
  <div class="box ">Box</div>
  <div class="card ctd">Card</div>
</div>

<style style lang="postcss">
/* your styles go here */
.ctd {
  background-color: var(--primary-color);
  color: var(--primary);
}
</style>

<script>
import Box from "$lib/Box.svelte";

// your script goes here
let title = "";
let prefix = "";
let url = "";
let image = "";
</script>
