<script>
  import { onMount, onDestroy } from "svelte";

  const reviews = [
    {
      name: "Bu Lina Prasetya",
      comment:
        "Mulai dari konsultasi hingga pengeboran, semuanya dilayani dengan baik. Hasil airnya jernih dan melimpah. Terima kasih Rebor Pro!",
      rating: 5,
    },
    {
      name: "Pak Dedi Nugroho",
      comment:
        "Awalnya ragu, tapi setelah lihat hasilnya, luar biasa! Air langsung keluar deras dan bening. Tim sangat profesional.",
      rating: 5,
    },
    {
      name: "Ibu Kartika Dewi",
      comment:
        "Pengerjaan cepat dan bersih. Harga juga transparan tanpa biaya tambahan. Saya sangat merekomendasikan!",
      rating: 5,
    },
    {
      name: "Pak Hendra Saputra",
      comment:
        "Hasil pengeborannya memuaskan. Air tidak bau besi dan sangat layak konsumsi. Prosesnya juga sesuai jadwal.",
      rating: 4.5,
    },
    {
      name: "Ibu Mega Sari",
      comment:
        "Saya suka karena ada edukasi tentang kedalaman dan kualitas air. Timnya informatif dan ramah!",
      rating: 5,
    },
    {
      name: "Pak Ahmad Fauzi",
      comment:
        "Sumur bor cepat selesai dalam sehari. Alat lengkap dan pengerjaan profesional. Tidak kecewa!",
      rating: 5,
    },
    {
      name: "Ibu Desi Ramadhani",
      comment:
        "Tim datang tepat waktu dan sangat cekatan. Air sumur langsung bisa dipakai. Pelayanan mantap!",
      rating: 5,
    },
    {
      name: "Pak Roni Taufik",
      comment:
        "Harga bersaing tapi kualitas kerja sangat memuaskan. Sudah saya rekomendasikan ke tetangga.",
      rating: 5,
    },
    {
      name: "Ibu Rika Marlina",
      comment:
        "Airnya deras dan tidak keruh. Sumur bor dibuat dengan rapi, lokasi kerja juga dibersihkan setelah selesai.",
      rating: 5,
    },
    {
      name: "Pak Bambang Suryono",
      comment:
        "Saya senang karena teknisinya komunikatif dan menjelaskan prosesnya dengan jelas. Hasilnya pun sangat baik.",
      rating: 4.5,
    },
    {
      name: "Ibu Sari Indah",
      comment:
        "Pelayanan luar biasa! Dari awal konsultasi hingga selesai, tim Rebor Pro sangat membantu dan profesional. Air sumur sekarang jernih dan melimpah, membuat hidup kami lebih mudah. Sangat direkomendasikan!",
      rating: 5,
    },
    {
      name: "Pak Joko",
      comment:
        "Hasil pengeboran melebihi ekspektasi saya. Airnya deras, bening, dan tidak ada bau apapun. Proses cepat dan harga transparan. Terima kasih atas pelayanan prima!",
      rating: 5,
    },
    {
      name: "Ibu Maya Sari",
      comment:
        "Tim yang sangat ahli dan ramah. Mereka memberikan edukasi yang berguna tentang sumur bor, dan hasilnya sungguh memuaskan. Air langsung bisa diminum tanpa perlu filter tambahan. Puas sekali!",
      rating: 5,
    },
    {
      name: "Pak Agus Setiawan",
      comment:
        "Pengalaman terbaik dengan jasa pengeboran. Pengerjaan rapi, lokasi dibersihkan sempurna, dan airnya melimpah ruah. Sudah saya ceritakan ke keluarga dan teman-teman. Mantap!",
      rating: 4.5,
    },
    {
      name: "Ibu Fitriani",
      comment:
        "Rebor Pro benar-benar solusi tepat untuk masalah air di rumah saya. Konsultasi gratis, proses cepat, dan hasilnya luar biasa. Air jernih dan sehat. Terima kasih banyak!",
      rating: 5,
    },
    {
      name: "Pak Rahman Hakim",
      comment:
        "Profesional dari awal hingga akhir. Tim datang tepat waktu, bekerja efisien, dan memberikan penjelasan yang jelas. Air sumur sekarang menjadi sumber kehidupan yang handal. Rekomendasi penuh!",
      rating: 5,
    },
    {
      name: "Ibu Dewi Lestari",
      comment:
        "Saya sangat terkesan dengan kualitas kerja Rebor Pro. Pengeboran dilakukan dengan presisi tinggi, hasil air melimpah dan berkualitas. Harga juga sangat kompetitif. Akan pakai lagi jika perlu!",
      rating: 5,
    },
    {
      name: "Pak Surya Pratama",
      comment:
        "Pelayanan yang cepat dan berkualitas. Dari survei hingga pengeboran, semuanya lancar tanpa kendala. Airnya bening dan tidak keruh. Tim sangat komunikatif dan membantu. Bagus sekali!",
      rating: 4.5,
    },
    {
      name: "Ibu Nurul Hidayah",
      comment:
        "Terima kasih Rebor Pro atas sumur bor yang fantastis! Air melimpah, proses bersih, dan tim yang sangat profesional. Sekarang rumah saya tidak pernah kekurangan air. Puas 100%!",
      rating: 5,
    },
    {
      name: "Pak Arif Rahman",
      comment:
        "Pelayanan top! Sumur bor selesai dalam waktu singkat, airnya jernih dan melimpah. Tim sangat kompeten dan harga sangat terjangkau. Akan rekomendasikan ke semua orang!",
      rating: 5,
    },
    {
      name: "Ibu Siti Aminah",
      comment:
        "Luar biasa! Dari konsultasi hingga hasil akhir, semuanya sempurna. Air sumur sekarang menjadi sumber air utama yang handal dan sehat. Terima kasih atas dedikasi timnya!",
      rating: 5,
    },
    {
      name: "Pak Budi Santoso",
      comment:
        "Hasil pengeboran melebihi harapan. Air deras, bening, dan tanpa bau. Proses profesional, lokasi kerja dibersihkan rapi. Pelayanan terbaik yang pernah saya alami!",
      rating: 5,
    },
    {
      name: "Ibu Laila Kusuma",
      comment:
        "Rebor Pro adalah pilihan tepat untuk sumur bor. Tim ahli, edukasi yang diberikan sangat membantu, dan hasilnya sungguh memuaskan. Air melimpah ruah setiap hari!",
      rating: 5,
    },
    {
      name: "Pak Eko Prasetyo",
      comment:
        "Profesional dan cepat. Pengeboran dilakukan dengan presisi, air langsung keluar deras. Harga transparan, tidak ada biaya tersembunyi. Sangat puas dan akan pakai lagi!",
      rating: 5,
    },
    {
      name: "Ibu Rina Sari",
      comment:
        "Tim yang sangat ramah dan informatif. Mereka menjelaskan setiap langkah dengan jelas. Hasil sumur bor fantastis, air jernih dan sehat. Rekomendasi penuh dari saya!",
      rating: 5,
    },
    {
      name: "Pak Hadi Wibowo",
      comment:
        "Pengalaman luar biasa dengan Rebor Pro. Pengerjaan rapi, cepat, dan hasil air melimpah. Sudah saya ceritakan ke keluarga besar. Terima kasih atas pelayanan prima!",
      rating: 5,
    },
    {
      name: "Ibu Maya Putri",
      comment:
        "Air sumur sekarang menjadi solusi utama untuk kebutuhan air rumah tangga. Pelayanan cepat, tim profesional, dan harga kompetitif. Puas sekali dengan hasilnya!",
      rating: 5,
    },
    {
      name: "Pak Teguh Setiawan",
      comment:
        "Rebor Pro benar-benar ahli di bidangnya. Dari survei hingga pengeboran, semuanya lancar. Airnya deras dan berkualitas tinggi. Akan rekomendasikan tanpa ragu!",
      rating: 5,
    },
    {
      name: "Ibu Dian Anggraini",
      comment:
        "Terima kasih atas sumur bor yang luar biasa! Tim datang tepat waktu, bekerja efisien, dan memberikan hasil yang memuaskan. Air melimpah dan sehat. Mantap!",
      rating: 5,
    },
    {
      name: "Pak Ferry Gunawan",
      comment:
        "Pelayanan terbaik! Sumur bor selesai sesuai jadwal, air jernih tanpa keruh, dan prosesnya sangat bersih. Harga juga sangat wajar. Puas 100%!",
      rating: 5,
    },
    {
      name: "Ibu Sari Melati",
      comment:
        "Rebor Pro membuat hidup saya lebih mudah dengan air sumur yang melimpah. Tim profesional, komunikatif, dan hasilnya melebihi ekspektasi. Terima kasih banyak!",
      rating: 5,
    },
    {
      name: "Pak Andi Saputra",
      comment:
        "Hasil pengeboran fantastis! Air deras, bening, dan langsung bisa diminum. Proses cepat dan rapi. Sudah saya rekomendasikan ke teman-teman. Bagus sekali!",
      rating: 5,
    },
    {
      name: "Ibu Nia Rahayu",
      comment:
        "Tim yang sangat membantu dan ahli. Edukasi tentang sumur bor sangat berguna, dan hasilnya sungguh memuaskan. Air melimpah ruah setiap saat. Puas sekali!",
      rating: 5,
    },
    {
      name: "Pak Dimas Pratama",
      comment:
        "Puas sekali dengan hasilnya!",
      rating: 5,
    },
  ];

  let currentPage = 0;
  const perPage = 4;
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
      name,
    )}&background=0D8ABC&color=fff&rounded=true`;
</script>

<!-- <section class="bg-white py-20 px-6 md:px-12"> -->
<section class="py-16 px-6 md:px-12">
  <div class="text-center mb-10">
    <h2 class="text-3xl font-bold text-gray-800 mb-2">Testimoni Pelanggan</h2>
    <p class="text-gray-600 max-w-xl mx-auto">
      Apa kata mereka yang sudah memakai jasa pengeboran air dari kami?
    </p>
  </div>

  <div class="max-w-6xl mx-auto">
    <div class="grid gap-6 sm:grid-cols-1 md:grid-cols-2">
      {#each reviews.slice(currentPage * perPage, currentPage * perPage + perPage) as r}
        <div
          class="bg-gradient-to-br from-blue-50 to-indigo-50 p-6 rounded-2xl shadow-md hover:shadow-lg transition duration-300"
        >
          <div class="flex items-center gap-4 mb-4">
            <img
              src={getAvatar(r.name)}
              alt={r.name}
              class="w-14 h-14 rounded-full object-cover ring-2 ring-blue-200"
            />
            <div>
              <h3 class="text-lg font-semibold text-gray-800">{r.name}</h3>
              <div class="flex">
                {#each Array(5) as _, i}
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill={i < Math.floor(r.rating) ||
                    (i === Math.floor(r.rating) && r.rating % 1 !== 0)
                      ? "currentColor"
                      : "none"}
                    viewBox="0 0 24 24"
                    stroke={i < r.rating ? "none" : "currentColor"}
                    class="w-5 h-5 text-yellow-400 drop-shadow-yellow-200"
                    style={i === Math.floor(r.rating) && r.rating % 1 !== 0
                      ? "clip-path: inset(0 50% 0 0);"
                      : ""}
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
                    />
                  </svg>
                {/each}
              </div>
            </div>
          </div>
          <p class="text-gray-700 text-sm leading-relaxed italic">
            "{r.comment}"
          </p>
        </div>
      {/each}
    </div>

    <!-- Navigasi Manual -->
    <div class="flex justify-between items-center mt-8">
      <button
        on:click={prevPage}
        class="bg-blue-100 text-blue-700 px-4 py-2 rounded-lg font-semibold hover:bg-blue-200 transition"
      >
        ← Sebelumnya
      </button>
      <span class="text-sm text-gray-500"
        >Halaman {currentPage + 1} / {totalPages}</span
      >
      <button
        on:click={nextPage}
        class="bg-blue-100 text-blue-700 px-4 py-2 rounded-lg font-semibold hover:bg-blue-200 transition"
      >
        Selanjutnya →
      </button>
    </div>
  </div>
</section>
