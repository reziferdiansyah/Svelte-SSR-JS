<script>
  import Testimonials from "$lib/components/Testimonials.svelte";
  import Carousel from "$lib/components/Carousel.svelte";
  import Features from "$lib/components/Features.svelte";

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
      title: "Konsultasi & survei lokasi",
      desc: "Survey titik air dengan teknisi ahli sebelum pengeboran.",
      icon: "📍",
    },
  ];
</script>

<!-- Carousel Hero -->
<Carousel />

<!-- Layanan -->
<section id="layanan" class="py-20 px-6 md:px-12 bg-gradient-to-br from-blue-50 to-indigo-50">
  <div class="text-center mb-12">
    <h2 class="text-3xl font-bold text-gray-800 mb-2">Layanan Kami</h2>
    <p class="text-gray-600">
      Kami melayani berbagai kebutuhan pengeboran air bersih.
    </p>
  </div>

  <div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">
    {#each services as s}
      <div
        class="bg-white p-6 rounded-2xl shadow hover:shadow-lg transition text-center border border-blue-200"
      >
        <div class="text-4xl mb-4 text-blue-500">{s.icon}</div>
        <h3 class="text-xl font-semibold text-blue-800 mb-2">{s.title}</h3>
        <p class="text-gray-600">{s.desc}</p>
      </div>
    {/each}
  </div>
</section>

<!-- Keunggulan -->
<Features />

<!-- Testimoni -->
<Testimonials />

<!-- CTA Hubungi -->
<section class="py-16 px-6 md:px-12  text-center">
  <h2 class="text-3xl font-bold text-blue-800 mb-4">Hubungi Kami Sekarang</h2>
  <p class="text-blue-800 mb-8">
    Dapatkan konsultasi gratis dan penawaran terbaik untuk kebutuhan sumur bor
    Anda.
  </p>
  <a
    href="/contact"
    class="bg-gradient-to-r from-green-600 to-blue-600 text-white px-8 py-4 rounded-xl font-semibold hover:from-green-700 hover:to-blue-700 transition"
    >Hubungi Kami</a
  >
</section>
