<script>
  import Header from "$lib/components/Header.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import "../app.css";
  export let data;
</script>

<svelte:head>
  <title>{data.meta?.title ?? 'MySite'}</title>
  <meta name="description" content={data.meta?.description ?? 'Welcome to MySite, your source for high-quality services.'} />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta charset="utf-8" />
</svelte:head>

<Header />
<slot />
<Footer />
