<script>
  import Header from "$lib/components/Header.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import "../app.css";
  export let data;
</script>

<svelte:head>
  <title>{data.meta?.title ?? 'Rebor Pro'}</title>
  <meta name="description" content={data.meta?.description ?? 'Welcome to Rebor Pro, your source for high-quality services.'} />
  <meta name="keywords" content={data.meta?.keywords ?? 'Rebor Pro, services, high-quality'} />
  <meta name="author" content="Rebor Pro" />
  <meta name="robots" content="index, follow" />
  <link rel="canonical" href={data.meta?.canonical ?? 'https://reborpro.com'} />

  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website" />
  <meta property="og:url" content={data.meta?.canonical ?? 'https://reborpro.com'} />
  <meta property="og:title" content={data.meta?.title ?? 'Rebor Pro'} />
  <meta property="og:description" content={data.meta?.description ?? 'Welcome to Rebor Pro, your source for high-quality services.'} />
  <meta property="og:image" content={data.meta?.ogImage ?? 'https://reborpro.com/images/og-image.jpg'} />

  <!-- Twitter -->
  <meta property="twitter:card" content="summary_large_image" />
  <meta property="twitter:url" content={data.meta?.canonical ?? 'https://reborpro.com'} />
  <meta property="twitter:title" content={data.meta?.title ?? 'Rebor Pro'} />
  <meta property="twitter:description" content={data.meta?.description ?? 'Welcome to Rebor Pro, your source for high-quality services.'} />
  <meta property="twitter:image" content={data.meta?.ogImage ?? 'https://reborpro.com/images/og-image.jpg'} />

  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta charset="utf-8" />
</svelte:head>

<Header />
<div class="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100">
<slot />
</div>
<Footer />
