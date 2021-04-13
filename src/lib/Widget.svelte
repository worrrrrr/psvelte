<!-- Widget.svelte -->

<div class="container">
  <slot name="title">No title was provided</slot>
  <p on:click="{() => (isShowing = !isShowing)}"></p>

  <slot name="footer" />
</div>

<style>
.container {
  color: black;
  border: 3px solid -color--primary;
}
</style>

<script>
let isShowing = true;
function toggle() {
  isShowing = !isShowing;
}
</script>
