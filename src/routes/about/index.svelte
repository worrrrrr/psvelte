<Widget>
  <h1 slot="title">header</h1>
  <h3>
    <pre>
      {JSON.stringify(data, null, 2)}
    </pre>
  </h3>
  <p slot="footer">Form Result</p>
</Widget>

<script>
import { onMount } from "svelte";
import Widget from "$lib/Widget.svelte";
let data;
onMount(async () => {
  data = await fetch(
    "https://api.coindesk.com/v1/bpi/currentprice.json"
  ).then((x) => x.json());
});
</script>
