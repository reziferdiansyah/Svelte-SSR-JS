<script>
  let isOpen = false;
  function toggleMenu() {
    isOpen = !isOpen;
  }
</script>

<header class="bg-white shadow-md sticky top-0 z-50">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between items-center h-16">
      <!-- Logo -->
      <div class="flex-shrink-0 text-xl font-bold text-blue-600">MySite</div>

      <!-- Desktop Menu -->
      <nav class="hidden md:flex space-x-4">
        <a href="/" class="text-gray-700 hover:text-blue-600">Beranda</a>
        <a href="/about" class="text-gray-700 hover:text-blue-600"
          >Tentang Kami</a
        >
        <a href="/contact" class="text-gray-700 hover:text-blue-600">Kontak</a>
      </nav>

      <!-- Mobile Menu Button -->
      <div class="md:hidden">
        <button
          on:click={toggleMenu}
          class="text-gray-700 hover:text-blue-600 focus:outline-none"
        >
          <svg
            class="w-6 h-6"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
          >
            {#if isOpen}
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            {:else}
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            {/if}
          </svg>
        </button>
      </div>
    </div>
  </div>

  <!-- Mobile Menu -->
  {#if isOpen}
    <div class="md:hidden bg-white shadow">
      <nav class="px-2 pt-2 pb-4 space-y-1">
        <a
          href="/"
          class="block px-3 py-2 text-gray-700 hover:bg-blue-100 rounded"
          >Beranda</a
        >
        <a
          href="/about"
          class="block px-3 py-2 text-gray-700 hover:bg-blue-100 rounded"
          >Tentang Kami</a
        >
        <a
          href="/contact"
          class="block px-3 py-2 text-gray-700 hover:bg-blue-100 rounded"
          >Kontak</a
        >
      </nav>
    </div>
  {/if}
</header>
