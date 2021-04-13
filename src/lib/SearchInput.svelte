<!-- markup (zero or more items) goes here -->

<slot name="input">
  <input type="search" bind:value  placeholder="Search.." />
</slot>
<slot name="output">
  {#each linkResult as link}
    <!-- content here -->
    <p>
      {JSON.stringify(link.item)}
      {link.score}
    </p>
  {/each}
</slot>

<style>
/* your styles go here */
input[type="search"] {
  width: 130px;
  -webkit-transition: width 0.4s ease-in-out;
  transition: width 0.4s ease-in-out;
}

/* When the input field gets focus, change its width to 100% */
input[type="search"]:focus {
  width: 100%;
}
</style>

<!--  key with name title -->
<script>
import Fuse from "fuse.js";
import linklist from "./db.json";
let value = "";

const fuse = new Fuse(linklist, {
  keys: ["name", "title", "url"],
  includeScore: true,
});
$: linkResult = fuse.search(value);
</script>
