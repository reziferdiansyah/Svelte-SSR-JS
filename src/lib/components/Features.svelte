<script lang="ts">
  const features = [
    "Tenaga ahli berpengalaman",
    "Proses pengerjaan cepat & rapi",
    "Peralatan modern & aman",
    "Harga bersaing dan transparan",
    "Garansi hasil pengeboran",
    "Hasil air jernih & berkualitas",
    "Layanan konsultasi gratis",
    "Dukungan pelanggan 24/7",
    "Solusi tepat sesuai kebutuhan",
    "Komitmen pada kepuasan pelanggan",
  ];
</script>

<section class="py-20 px-6 md:px-12 bg-gradient-to-b from-white to-blue-25">
  <div class="max-w-4xl mx-auto text-center">
    <h2 class="text-3xl font-bold text-blue-800 mb-6">Kenapa Memilih Kami?</h2>
    <ul
      class="grid grid-cols-1 sm:grid-cols-2 gap-6 text-left text-gray-800 text-lg"
    >
      {#each features as f}
        <li class="flex items-start gap-3">
          <span class="text-green-500 text-2xl drop-shadow-sm">✔️</span>
          <span>{f}</span>
        </li>
      {/each}
    </ul>
  </div>
</section>
