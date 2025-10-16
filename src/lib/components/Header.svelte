<script>
  import { page } from '$app/stores';

  let isOpen = false;
  function toggleMenu() {
    isOpen = !isOpen;
  }
</script>

<header class="bg-gradient-to-r from-white to-blue-50 shadow-md text-textutama sticky top-0 z-50">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between items-center h-16">
      <!-- Logo -->
      <div class="flex-shrink-0 text-xl font-bold text-blue-700">MySite</div>

      <!-- Desktop Menu -->
      <nav class="hidden md:flex space-x-4">
        <a href="/" class="hover:text-blue-600 hover:underline transition {$page.url.pathname === '/' ? 'text-blue-600 underline' : ''}">Beranda</a>
        <a href="/about" class="hover:text-blue-600 hover:underline transition {$page.url.pathname === '/about' ? 'text-blue-600 underline' : ''}"
          >Tentang Kami</a
        >
        <a href="/testimoni" class="hover:text-blue-600 hover:underline transition {$page.url.pathname === '/testimoni' ? 'text-blue-600 underline' : ''}"
          >Testimoni</a
        >
        <a href="/contact" class="hover:text-blue-600 hover:underline transition {$page.url.pathname === '/contact' ? 'text-blue-600 underline' : ''}">Kontak</a>
      </nav>

      <!-- Mobile Menu Button -->
      <div class="md:hidden">
        <button
          on:click={toggleMenu}
          class="text-gray-700 hover:text-blue-600 focus:outline-none transition"
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
    <div class="md:hidden bg-white shadow border-t border-blue-200">
      <nav class="px-2 pt-2 pb-4 space-y-1">
        <a
          href="/"
          class="block px-3 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded transition {$page.url.pathname === '/' ? 'text-blue-600 underline' : ''}"
          >Beranda</a
        >
        <a
          href="/about"
          class="block px-3 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded transition {$page.url.pathname === '/about' ? 'text-blue-600 underline' : ''}"
          >Tentang Kami</a
        >
          <a
          href="/testimoni"
          class="block px-3 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded transition {$page.url.pathname === '/testimoni' ? 'text-blue-600 underline' : ''}"
          >Testimoni</a
        >
        <a
          href="/contact"
          class="block px-3 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded transition {$page.url.pathname === '/contact' ? 'text-blue-600 underline' : ''}"
          >Kontak</a
        >
      </nav>
    </div>
  {/if}
</header>
