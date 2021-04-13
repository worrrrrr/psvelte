<div class="grid-container">
  <div class="top topbar">
    <Nav />
  </div>
  <div class="mid"><slot /></div>
  <div class="btm">Footer</div>
</div>

<style lang="postcss">
.topbar {
  position: -webkit-sticky;
}
.grid-container {
  height: 100vh;
  width: 100%;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 10% 1fr 10%;
  gap: 0px 0px;
  grid-template-areas:
    "top"
    "mid"
    "btm";
}

.top {
  grid-area: top;
}

.mid {
  grid-area: mid;
}

.btm {
  grid-area: btm;
}

@media all and (-ms-high-contrast: none) {
  .grid-container {
    display: -ms-grid;
    -ms-grid-columns: 1fr;
    -ms-grid-rows: 10% 1fr 10%;
  }

  .top {
    -ms-grid-row: 1;
    -ms-grid-row-span: 1;
    -ms-grid-column: 1;
    -ms-grid-column-span: 1;
  }

  .mid {
    display: -ms-grid;
    -ms-grid-columns: repeat(8, 1fr);
    -ms-grid-rows: repeat(6, 1fr);
    -ms-grid-row: 2;
    -ms-grid-row-span: 1;
    -ms-grid-column: 1;
    -ms-grid-column-span: 1;
  }

  .btm {
    -ms-grid-row: 3;
    -ms-grid-row-span: 1;
    -ms-grid-column: 1;
    -ms-grid-column-span: 1;
  }
}
</style>

<script>
import Nav from "$lib/Nav.svelte";
</script>
