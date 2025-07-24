<script>
  import Carousel from "$lib/components/Carousel.svelte";
</script>

<main class="min-h-screen bg-white">
  <!-- WhatsApp Icon fixed on left -->
  <a
    href="https://wa.me/1234567890"
    target="_blank"
    rel="noopener noreferrer"
    aria-label="WhatsApp"
    class="fixed left-4 top-1/2 transform -translate-y-1/2 bg-green-500 hover:bg-green-600 text-white p-3 rounded-full shadow-lg z-50"
  >
    <svg
      width="20"
      height="19"
      viewBox="0 0 20 19"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M5.30005 0.999951C4.90005 0.199951 4.60005 0.199951 4.20005 0.199951C3.90005 0.199951 3.60005 0.199951 3.30005 0.199951C3.00005 0.199951 2.50005 0.299952 2.00005 0.799952C1.60005 1.29995 0.300049 2.39995 0.300049 4.79995C0.300049 7.19995 2.00005 9.39995 2.20005 9.69995C2.40005 9.99995 5.50005 15 10.3 16.9C14.3 18.5 15.1 18.1999 16 18.0999C16.9 17.9999 18.8001 17 19.2001 15.8C19.6001 14.7 19.6 13.7 19.5 13.5C19.4 13.3 19.1 13.2 18.6 12.9C18.1 12.6 15.8 11.5 15.4 11.4C15 11.2 14.6 11.2 14.3 11.6C14 12.1 13.1 13.1 12.8 13.5C12.5 13.8 12.2 13.9 11.8 13.6C11.3 13.4 9.80005 12.9 8.00005 11.2C6.60005 9.89995 5.60005 8.39995 5.40005 7.89995C5.10005 7.39995 5.40005 7.19995 5.60005 6.89995C5.80005 6.69995 6.10005 6.29995 6.30005 6.09995C6.50005 5.79995 6.60005 5.59995 6.80005 5.29995C7.00005 4.99995 6.90005 4.69995 6.80005 4.49995C6.60005 4.29995 5.70005 1.99995 5.30005 0.999951Z"
        fill="white"
      />
    </svg>
  </a>

  <!-- Carousel section -->
  <section>
    <Carousel />
  </section>

  <!-- Additional scrollable content -->
  <section class="py-16 px-4 text-center bg-gray-50">
    <h2 class="text-3xl font-bold mb-6">About Us</h2>
    <p class="max-w-2xl mx-auto text-gray-600">
      MySite is dedicated to providing high-quality services that help you
      achieve your goals. We believe in simplicity, efficiency, and great user
      experience.
    </p>
  </section>

  <section class="py-16 px-4 text-center bg-white">
    <h2 class="text-3xl font-bold mb-6">Our Services</h2>
    <div
      class="max-w-5xl mx-auto grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8"
    >
      <div class="bg-gray-100 p-6 rounded-lg shadow hover:shadow-md transition">
        <h3 class="text-xl font-semibold mb-2">Web Development</h3>
        <p class="text-gray-600">Build fast and modern web apps with us.</p>
      </div>
      <div class="bg-gray-100 p-6 rounded-lg shadow hover:shadow-md transition">
        <h3 class="text-xl font-semibold mb-2">UI/UX Design</h3>
        <p class="text-gray-600">Design experiences users love.</p>
      </div>
      <div class="bg-gray-100 p-6 rounded-lg shadow hover:shadow-md transition">
        <h3 class="text-xl font-semibold mb-2">Consulting</h3>
        <p class="text-gray-600">We help you make the right tech decisions.</p>
      </div>
    </div>
  </section>

  <section class="py-16 px-4 text-center bg-gray-50">
    <h2 class="text-3xl font-bold mb-6">Contact</h2>
    <p class="text-gray-600">
      Feel free to reach out via email or our contact form.
    </p>
    <button
      class="mt-4 px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition"
    >
      Get in Touch
    </button>
  </section>
</main>
