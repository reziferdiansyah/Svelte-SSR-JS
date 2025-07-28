<script>
  const phone = "6281234567890";
  const message = "Halo, saya tertarik dengan layanan sumur bor Anda.";
  const whatsappURL = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
</script>

<a
  href={whatsappURL}
  target="_blank"
  rel="noopener noreferrer"
  class="fixed bottom-4 left-4 z-50 flex items-center gap-3 px-5 py-3 rounded-full bg-green-600 hover:bg-green-700 text-white shadow-lg transition-all duration-300 hover:scale-105"
  aria-label="Kirim WhatsApp"
>
  <!-- Icon WhatsApp -->
 <svg
    class="w-6 h-6 text-white"
    fill="currentColor"
    viewBox="0 0 24 24"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M20.52 3.48A11.913 11.913 0 0012 0C5.37 0 .02 5.37.02 12c0 2.11.55 4.18 1.59 6.02L0 24l6.09-1.58A11.96 11.96 0 0012 24c6.63 0 12-5.37 12-12 0-3.19-1.24-6.19-3.48-8.52zM12 22.08a10.035 10.035 0 01-5.11-1.41l-.36-.21-3.61.93.96-3.52-.24-.37a10.046 10.046 0 01-1.56-5.5C2.08 6.08 6.08 2.08 12 2.08s9.92 4 9.92 9.92-4 9.92-9.92 9.92zm5.4-7.26c-.3-.15-1.77-.87-2.04-.97-.27-.1-.46-.15-.66.15-.2.3-.76.97-.93 1.17-.17.2-.34.22-.64.07-.3-.15-1.27-.47-2.42-1.5a9.208 9.208 0 01-1.7-2.1c-.18-.3-.02-.47.13-.62.13-.13.3-.34.45-.5.15-.17.2-.3.3-.5.1-.2.05-.37-.03-.52-.08-.15-.66-1.6-.91-2.2-.24-.6-.48-.52-.66-.53-.17-.01-.37-.02-.57-.02-.2 0-.52.07-.8.37s-1.05 1.02-1.05 2.5c0 1.47 1.08 2.9 1.23 3.1.15.2 2.13 3.26 5.17 4.57 3.04 1.31 3.04.87 3.58.82.54-.05 1.77-.72 2.02-1.42.25-.7.25-1.3.17-1.42-.08-.13-.27-.2-.57-.35z"
    />
  </svg>

  <!-- Label -->
  <span class="sm:inline text-sm font-semibold tracking-wide">
      Konsultasi Gratis
  </span>
</a>
