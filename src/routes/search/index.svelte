<!-- markup (zero or more items) goes here -->
<div class="mid">
  <SearchInput>
    <Box>
      <h1>{title}</h1>
      <h3>{description}</h3>
      <p>
        {url}
      </p>
    </Box>
  </SearchInput>
</div>

<style>
/* your styles go here */
</style>

<script>
import Box from "$lib/Box.svelte";

import FileInput from "$lib/FileInput.svelte";
import SearchInput from "$lib/SearchInput.svelte";

let title;
let url;
let description;
let user;
let image;
</script>
