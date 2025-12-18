<script lang="ts">
  import { onMount } from 'svelte';

  onMount(() => {
    // Inisialisasi jika diperlukan
  });
</script>

<section class="bg-gradient-to-br from-blue-50 to-indigo-100 py-16 px-6 md:px-12 min-h-screen">
  <div class="max-w-6xl mx-auto">
    <div class="text-center mb-12">
      <h1 class="text-5xl font-bold text-gray-800 mb-4">Hubungi Kami</h1>
      <p class="text-gray-600 text-xl max-w-2xl mx-auto">
        Siap membantu kebutuhan sumur bor Anda dengan layanan profesional dan berkualitas tinggi. Kirim pesan atau hubungi langsung kami untuk konsultasi gratis!
      </p>
    </div>

      <!-- Info Kontak -->
      <div class="text-gray-700 grid grid-cols-1 md:grid-cols-2 gap-6">
        <div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-4">
            <svg class="w-8 h-8 text-blue-600 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
            </svg>
            <h3 class="text-2xl font-semibold">Alamat</h3>
          </div>
          <p class="text-lg">Jl. Sumber Air No. 123, Jakarta Selatan, Indonesia</p>
          <p class="text-sm text-gray-500 mt-2">Kunjungi kantor kami untuk konsultasi tatap muka</p>
        </div>

        <div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-4">
            <svg class="w-8 h-8 text-green-600 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
            </svg>
            <h3 class="text-2xl font-semibold">Telepon & WhatsApp</h3>
          </div>
          <p class="text-lg">
            Telepon: <a href="tel:+6281234567890" class="text-blue-600 hover:underline font-medium">0812-3456-7890</a><br />
            WhatsApp: <a href="https://wa.me/6281234567890" target="_blank" class="text-green-600 hover:underline font-medium">Chat via WhatsApp</a>
          </p>
          <p class="text-sm text-gray-500 mt-2">Tersedia 24/7 untuk keadaan darurat</p>
        </div>

        <div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-4">
            <svg class="w-8 h-8 text-red-600 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 4.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
            </svg>
            <h3 class="text-2xl font-semibold">Email</h3>
          </div>
          <p class="text-lg">
            <a href="mailto:info@sumurborpro.id" class="text-blue-600 hover:underline font-medium">info@sumurborpro.id</a>
          </p>
          <p class="text-sm text-gray-500 mt-2">Balas email dalam 24 jam</p>
        </div>

        <div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-4">
            <svg class="w-8 h-8 text-purple-600 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
            </svg>
            <h3 class="text-2xl font-semibold">Jam Operasional</h3>
          </div>
          <p class="text-lg">
            Senin - Minggu : 08:00 - 17:00<br />
          </p>
          <p class="text-sm text-gray-500 mt-2">Diluar jam operasional, hubungi WhatsApp</p>
        </div>
      </div>

    
    <!-- Peta Lokasi (Placeholder) -->
    <div class="mt-16">
      <h3 class="text-3xl font-bold text-gray-800 text-center mb-8">Lokasi Kami</h3>
      <div class="bg-white p-4 rounded-2xl shadow-lg">
        <div class="aspect-w-16 aspect-h-9 rounded-lg">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.521260322283!2d106.816666!3d-6.208763!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f5d2e764b12d%3A0x3d2ad6e1e0e9fb1!2sJl.%20Sumber%20Air%20No.%20123%2C%20Jakarta%20Selatan%2C%20Indonesia!5e0!3m2!1sen!2sid!4v1690000000000!5m2!1sen!2sid" width="100%" height="100%" style="border:0;" allowfullscreen loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
      </div>
    </div>
  </div>
</section>
