<script>
  const team = [
    {
      name: "Ahmad Fauzi",
      role: "Teknisi Utama",
      image: "/images/ahmad.jpg",
    },
    {
      name: "Rina Sari",
      role: "Customer Support",
      image: "/images/rina.jpg",
    },
    {
      name: "Budi Hartono",
      role: "Operator Mesin",
      image: "/images/budi.jpg",
    },
  ];
</script>

<section class="bg-white py-16 px-6 md:px-12">
  <div class="max-w-6xl mx-auto text-center">
    <h2 class="text-4xl font-bold text-gray-800 mb-4">Tentang Kami</h2>
    <p class="text-gray-600 max-w-3xl mx-auto text-lg">
      Kami adalah tim profesional yang bergerak di bidang jasa pengeboran sumur,
      berpengalaman lebih dari <span class="font-semibold text-blue-600">10 tahun</span>
      melayani kebutuhan air bersih di berbagai daerah. Dengan peralatan modern dan tenaga ahli,
      kami berkomitmen memberikan hasil terbaik, cepat, dan terpercaya.
    </p>
  </div>

  <div class="mt-16 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8 max-w-5xl mx-auto">
    {#each team as member}
      <div class="bg-gray-50 p-6 rounded-2xl shadow-md hover:shadow-lg transition">
        <img src={member.image} alt={member.name} class="w-24 h-24 rounded-full mx-auto mb-4 object-cover"/>
        <h3 class="text-xl font-semibold text-gray-800">{member.name}</h3>
        <p class="text-blue-600">{member.role}</p>
      </div>
    {/each}
  </div>
</section>
