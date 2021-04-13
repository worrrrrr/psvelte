<h1>{slug}</h1>
<h3>{JSON.stringify(post)}</h3>

<script context="module">
export async function load(ctx) {
  let slug = ctx.page.params.slug;
  let post = { title: "post object" };
  return { props: { slug, post } };
}
</script>

<script>
export let slug;
export let post;
</script>
