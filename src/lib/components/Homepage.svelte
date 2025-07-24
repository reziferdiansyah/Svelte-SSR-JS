<script>
  import { onMount } from 'svelte';
  import Testimonials from '$lib/components/Testimonials.svelte';


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

  // Layanan
  const services = [
    {
      title: "Sumur Bor Dalam",
      desc: "Sumur air bersih untuk rumah, pabrik, hingga pertanian.",
      icon: "💧",
    },
    {
      title: "Servis & Perbaikan",
      desc: "Perbaikan pompa, pipa dan perawatan sistem sumur.",
      icon: "🔧",
    },
    {
      title: "Survey Lokasi",
      desc: "Survey titik air dengan teknisi ahli sebelum pengeboran.",
      icon: "📍",
    },
  ];

  // Fitur
  const features = [
    "Berpengalaman 10+ tahun di lapangan",
    "Tim profesional & bersertifikat",
    "Harga bersaing & transparan",
    "Proyek cepat, rapi & bergaransi",
  ];
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

<!-- Layanan -->
<section id="layanan" class="py-20 px-6 md:px-12 bg-gray-50">
  <div class="text-center mb-12">
    <h2 class="text-3xl font-bold text-gray-800 mb-2">Layanan Kami</h2>
    <p class="text-gray-600">Kami melayani berbagai kebutuhan pengeboran air bersih.</p>
  </div>

  <div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">
    {#each services as s}
      <div class="bg-white p-6 rounded-2xl shadow hover:shadow-lg transition text-center">
        <div class="text-4xl mb-4">{s.icon}</div>
        <h3 class="text-xl font-semibold text-gray-800 mb-2">{s.title}</h3>
        <p class="text-gray-600">{s.desc}</p>
      </div>
    {/each}
  </div>
</section>

<!-- Keunggulan -->
<section class="py-20 px-6 md:px-12 bg-white">
  <div class="max-w-4xl mx-auto text-center">
    <h2 class="text-3xl font-bold text-gray-800 mb-6">Kenapa Memilih Kami?</h2>
    <ul class="grid grid-cols-1 sm:grid-cols-2 gap-6 text-left text-gray-700 text-lg">
      {#each features as f}
        <li class="flex items-start gap-3">
          <span class="text-green-500 text-2xl">✔️</span>
          <span>{f}</span>
        </li>
      {/each}
    </ul>
  </div>
</section>

<Testimonials />

<!-- CTA Hubungi -->
<section class="py-16 px-6 md:px-12 bg-blue-100 text-center">
  <h2 class="text-3xl font-bold text-blue-700 mb-4">Hubungi Kami Sekarang</h2>
  <p class="text-blue-700 mb-8">Dapatkan konsultasi gratis dan penawaran terbaik untuk kebutuhan sumur bor Anda.</p>
  <a href="/contact" class="bg-blue-700 text-white px-8 py-4 rounded-xl font-semibold hover:bg-blue-800 transition">Hubungi Kami</a>
</section>
