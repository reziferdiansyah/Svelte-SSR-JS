<script>
  let name = '';
  let email = '';
  let message = '';

  const handleSubmit = () => {
    // Logika kirim formulir (bisa dihubungkan ke API/email)
    console.log({ name, email, message });
    alert('Pesan berhasil dikirim!');
    name = email = message = '';
  };
</script>

<section class="bg-blue-50 py-16 px-6 md:px-12">
  <div class="max-w-6xl mx-auto">
    <div class="text-center mb-12">
      <h2 class="text-4xl font-bold text-gray-800 mb-2">Hubungi Kami</h2>
      <p class="text-gray-600 text-lg">
        Siap membantu kebutuhan sumur bor Anda. Kirim pesan atau hubungi langsung kami!
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
      <!-- Formulir -->
      <form class="bg-white p-8 rounded-2xl shadow-md space-y-6" on:submit|preventDefault={handleSubmit}>
        <div>
          <label class="block text-sm font-medium text-gray-700">Nama Lengkap</label>
          <input type="text" bind:value={name} required class="w-full mt-1 p-3 border rounded-xl focus:ring focus:ring-blue-200" />
        </div>
        <div>
          <label class="block text-sm font-medium text-gray-700">Email</label>
          <input type="email" bind:value={email} required class="w-full mt-1 p-3 border rounded-xl focus:ring focus:ring-blue-200" />
        </div>
        <div>
          <label class="block text-sm font-medium text-gray-700">Pesan</label>
          <textarea bind:value={message} rows="5" required class="w-full mt-1 p-3 border rounded-xl focus:ring focus:ring-blue-200"></textarea>
        </div>
        <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 rounded-xl transition">
          Kirim Pesan
        </button>
      </form>

      <!-- Info Kontak -->
      <div class="text-gray-700 space-y-6">
        <div class="bg-white p-6 rounded-2xl shadow-md">
          <h3 class="text-xl font-semibold mb-2">Alamat Kantor</h3>
          <p>Jl. Sumber Air No. 123, Jakarta Selatan</p>
        </div>
        <div class="bg-white p-6 rounded-2xl shadow-md">
          <h3 class="text-xl font-semibold mb-2">Telepon & WhatsApp</h3>
          <p>
            Telp: <a href="tel:+6281234567890" class="text-blue-600 hover:underline">0812-3456-7890</a><br />
            WA: <a href="https://wa.me/6281234567890" target="_blank" class="text-green-600 hover:underline">Chat via WhatsApp</a>
          </p>
        </div>
        <div class="bg-white p-6 rounded-2xl shadow-md">
          <h3 class="text-xl font-semibold mb-2">Email</h3>
          <p>
            <a href="mailto:info@sumurborpro.id" class="text-blue-600 hover:underline">info@sumurborpro.id</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</section>
