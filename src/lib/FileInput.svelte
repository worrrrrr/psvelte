<div class="box">
  <label for="avatar">Upload a picture:</label>
  <input
    accept="image/png, image/jpeg"
    bind:files
    id="avatar"
    name="avatar"
    type="file"
  />
</div>
<div class="box">
  <label for="many">Upload multiple files of any type:</label>
  <input bind:files id="many" multiple type="file" />
</div>
{#if files}
  <h2>Selected files:</h2>
  {#each Array.from(files) as file}
    <img src="{file.url}" alt="{file} awesome" />
    <p>{file.name} ({file.size} bytes)</p>
  {/each}
{/if}

<script>
let files;
let src;

$: if (files) {
  // Note that `files` is of type `FileList`, not an Array:
  // https://developer.mozilla.org/en-US/docs/Web/API/FileList
  console.log(files);

  for (const file of files) {
    console.log(`${file.name}: ${file.size} bytes`);
  }
}
</script>
