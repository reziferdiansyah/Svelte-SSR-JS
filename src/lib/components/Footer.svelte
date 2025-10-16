<script>
  const year = new Date().getFullYear();
    import WhatsappFloatingButton from '$lib//components/WhatsappFloatingButton.svelte';
    import ScrollToTopButton from '$lib/components/ScrollToTopButton.svelte';


</script>
<WhatsappFloatingButton/>
<ScrollToTopButton/>
<footer class="bg-gradient-to-r from-cyan-500 to-blue-500 shadow-lg text-white py-10 px-6 md:px-12">
  <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">

    <!-- Brand / Deskripsi -->
    <div>
      <h2 class="text-2xl font-bold mb-3">SumurBorPro</h2>
      <p class="text-white">
        Layanan jasa sumur bor terpercaya sejak 2013. Siap membantu kebutuhan air bersih Anda dengan teknologi modern dan tim berpengalaman.
      </p>
    </div>

    <!-- Navigasi Cepat -->
    <div>
      <h3 class="text-xl font-semibold mb-3">Navigasi</h3>
      <ul class="space-y-2 text-white">
        <li><a href="/" class="hover:underline hover:text-cyan-200">Beranda</a></li>
        <li><a href="/about" class="hover:underline hover:text-cyan-200">Tentang Kami</a></li>
        <li><a href="/testimoni" class="hover:underline hover:text-cyan-200">Testimoni</a></li>
        <!-- <li><a href="/#layanan" class="hover:underline hover:text-cyan-200">Layanan</a></li> -->
        <li><a href="/contact" class="hover:underline hover:text-cyan-200">Kontak</a></li>
      </ul>
    </div>

    <!-- Kontak -->
    <div>
      <h3 class="text-xl font-semibold mb-3">Hubungi Kami</h3>
      <ul class="space-y-2 text-white text-sm">
        <li>📍 Jl. Sumber Air No. 123, Jakarta Selatan</li>
        <li>📞 <a href="tel:+6281234567890" class="hover:underline hover:text-cyan-200">0812-3456-7890</a></li>
        <li>✉️ <a href="mailto:info@sumurborpro.id" class="hover:underline hover:text-cyan-200">info@sumurborpro.id</a></li>
        <li>💬 <a href="https://wa.me/6281234567890" target="_blank" class="hover:underline text-green-300 hover:text-green-100">Chat via WhatsApp</a></li>
      </ul>
    </div>
  </div>

  <div class="mt-10 border-t border-white/30 pt-6 text-center text-white/70 text-sm">
    &copy; {year} SumurBorPro. All rights reserved.
  </div>
</footer>
