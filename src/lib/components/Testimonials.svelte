<script>
  import { onMount, onDestroy } from 'svelte';

  const reviews = [
  {
    "name": "Bu Lina Prasetya",
    "comment": "Mulai dari konsultasi hingga pengeboran, semuanya dilayani dengan baik. Hasil airnya jernih dan melimpah. Terima kasih SumurBorPro!",
    "rating": 5
  },
  {
    "name": "Pak Dedi Nugroho",
    "comment": "Awalnya ragu, tapi setelah lihat hasilnya, luar biasa! Air langsung keluar deras dan bening. Tim sangat profesional.",
    "rating": 5
  },
  {
    "name": "Ibu Kartika Dewi",
    "comment": "Pengerjaan cepat dan bersih. Harga juga transparan tanpa biaya tambahan. Saya sangat merekomendasikan!",
    "rating": 5
  },
  {
    "name": "Pak Hendra Saputra",
    "comment": "Hasil pengeborannya memuaskan. Air tidak bau besi dan sangat layak konsumsi. Prosesnya juga sesuai jadwal.",
    "rating": 4
  },
  {
    "name": "Ibu Mega Sari",
    "comment": "Saya suka karena ada edukasi tentang kedalaman dan kualitas air. Timnya informatif dan ramah!",
    "rating": 5
  },
  {
    "name": "Pak Ahmad Fauzi",
    "comment": "Sumur bor cepat selesai dalam sehari. Alat lengkap dan pengerjaan profesional. Tidak kecewa!",
    "rating": 5
  },
  {
    "name": "Ibu Desi Ramadhani",
    "comment": "Tim datang tepat waktu dan sangat cekatan. Air sumur langsung bisa dipakai. Pelayanan mantap!",
    "rating": 5
  },
  {
    "name": "Pak Roni Taufik",
    "comment": "Harga bersaing tapi kualitas kerja sangat memuaskan. Sudah saya rekomendasikan ke tetangga.",
    "rating": 5
  },
  {
    "name": "Ibu Rika Marlina",
    "comment": "Airnya deras dan tidak keruh. Sumur bor dibuat dengan rapi, lokasi kerja juga dibersihkan setelah selesai.",
    "rating": 5
  },
  {
    "name": "Pak Bambang Suryono",
    "comment": "Saya senang karena teknisinya komunikatif dan menjelaskan prosesnya dengan jelas. Hasilnya pun sangat baik.",
    "rating": 4
  }
];

  let currentPage = 0;
  const perPage = 2;
  const totalPages = Math.ceil(reviews.length / perPage);
  // @ts-ignore
  let interval;

  function nextPage() {
    currentPage = (currentPage + 1) % totalPages;
  }

  function prevPage() {
    currentPage = (currentPage - 1 + totalPages) % totalPages;
  }

  onMount(() => {
    interval = setInterval(nextPage, 7000); // ganti setiap 7 detik
  });

  onDestroy(() => {
    // @ts-ignore
    clearInterval(interval);
  });

  // @ts-ignore
  const getAvatar = (name) =>
    `https://ui-avatars.com/api/?name=${encodeURIComponent(
      name
    )}&background=0D8ABC&color=fff&rounded=true`;
</script>

<section class="bg-white py-20 px-6 md:px-12">
  <div class="text-center mb-10">
    <h2 class="text-3xl font-bold text-gray-800 mb-2">Testimoni Pelanggan</h2>
    <p class="text-gray-600 max-w-xl mx-auto">Apa kata mereka yang sudah memakai jasa pengeboran air dari kami?</p>
  </div>

  <div class="max-w-6xl mx-auto">
    <div class="grid gap-6 sm:grid-cols-1 md:grid-cols-2">
      {#each reviews.slice(currentPage * perPage, currentPage * perPage + perPage) as r}
        <div class="bg-blue-50 p-6 rounded-2xl shadow-md hover:shadow-lg transition duration-300">
          <div class="flex items-center gap-4 mb-4">
            <img src={getAvatar(r.name)} alt={r.name} class="w-14 h-14 rounded-full object-cover" />
            <div>
              <h3 class="text-lg font-semibold text-gray-800">{r.name}</h3>
              <div class="flex">
                {#each Array(5) as _, i}
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill={i < r.rating ? "currentColor" : "none"}
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    class="w-5 h-5 text-yellow-400"
                  >
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" />
                  </svg>
                {/each}
              </div>
            </div>
          </div>
          <p class="text-gray-700 text-sm leading-relaxed italic">"{r.comment}"</p>
        </div>
      {/each}
    </div>

    <!-- Navigasi Manual -->
    <div class="flex justify-between items-center mt-8">
      <button on:click={prevPage} class="text-blue-700 font-semibold hover:underline">
        ← Sebelumnya
      </button>
      <span class="text-sm text-gray-500">Halaman {currentPage + 1} / {totalPages}</span>
      <button on:click={nextPage} class="text-blue-700 font-semibold hover:underline">
        Selanjutnya →
      </button>
    </div>
  </div>
</section>
