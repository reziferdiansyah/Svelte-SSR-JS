<script>
  import Testimonials from '$lib/components/Testimonials.svelte';
  import Carousel from '$lib/components/Carousel.svelte';

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

<!-- Carousel Hero -->
<Carousel/>

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

<!-- Testimoni -->
<Testimonials />

<!-- CTA Hubungi -->
<section class="py-16 px-6 md:px-12 bg-blue-100 text-center">
  <h2 class="text-3xl font-bold text-blue-700 mb-4">Hubungi Kami Sekarang</h2>
  <p class="text-blue-700 mb-8">Dapatkan konsultasi gratis dan penawaran terbaik untuk kebutuhan sumur bor Anda.</p>
  <a href="/contact" class="bg-blue-700 text-white px-8 py-4 rounded-xl font-semibold hover:bg-blue-800 transition">Hubungi Kami</a>
</section>
