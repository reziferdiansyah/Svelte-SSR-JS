<script>
    import { onMount } from 'svelte';
  // Carousel
  let slides = [
    {
      title: "Jasa Sumur Bor Profesional",
      desc: "Melayani pengeboran air bersih untuk rumah, industri, dan pertanian.",
      image: "/images/sumur1.jpg",
    },
    {
      title: "Teknisi Ahli & Terpercaya",
      desc: "Lebih dari 10 tahun pengalaman di bidang pengeboran air tanah.",
      image: "/images/sumur2.jpg",
    },
    {
      title: "Hasil Cepat & Bergaransi",
      desc: "Menggunakan alat bor modern dengan akurasi tinggi.",
      image: "/images/sumur3.jpg",
    },
  ];
  let current = 0;
  const next = () => (current = (current + 1) % slides.length);
  const prev = () => (current = (current - 1 + slides.length) % slides.length);

  // @ts-ignore
  let interval;
  onMount(() => {
    interval = setInterval(next, 5000);
    // @ts-ignore
    return () => clearInterval(interval);
  });
</script>

<style>
  .carousel-img {
    background-size: cover;
    background-position: center;
  }
</style>

<!-- Carousel Hero -->
<section class="relative h-[500px] overflow-hidden">
  {#each slides as slide, i}
    <div
      class="absolute inset-0 transition-opacity duration-700 ease-in-out"
      class:hidden={i !== current}
    >
      <div
        class="w-full h-full carousel-img"
        style="background-image: url({slide.image})"
      >
        <div class="w-full h-full bg-black bg-opacity-60 flex items-center justify-center px-4">
          <div class="text-center text-white max-w-2xl">
            <h1 class="text-3xl md:text-5xl font-bold mb-4">{slide.title}</h1>
            <p class="text-lg md:text-xl mb-6">{slide.desc}</p>
            <a href="#layanan" class="bg-white text-blue-600 px-6 py-3 rounded-xl font-semibold hover:bg-blue-100 transition">Lihat Layanan</a>
          </div>
        </div>
      </div>
    </div>
  {/each}

  <!-- Navigasi -->
  <button on:click={prev} class="absolute left-4 top-1/2 -translate-y-1/2 text-white text-3xl hover:scale-110 transition">‹</button>
  <button on:click={next} class="absolute right-4 top-1/2 -translate-y-1/2 text-white text-3xl hover:scale-110 transition">›</button>

  <!-- Bullet -->
  <div class="absolute bottom-5 left-1/2 -translate-x-1/2 flex gap-2">
    {#each slides as _, i}
      <div
        class="w-3 h-3 rounded-full bg-white transition-opacity cursor-pointer"
        class:opacity-50={i !== current}
        on:click={() => (current = i)}
      />
    {/each}
  </div>
</section>
