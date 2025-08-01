<script>
  import { onMount } from 'svelte';
  // We'll use the 'fly' transition for the toast notification
  import { fly } from 'svelte/transition';

  // State variable to control the visibility of the pop-up
  let showPopup = false;
  // Variable for the name to be displayed
  

  // `onMount` is a Svelte lifecycle hook that runs after the component is first rendered.
  onMount(() => {
    // We use a slight delay to ensure the component is fully rendered before showing the pop-up.
    setTimeout(() => {
      showPopup = true;
    }, 500); // 500ms delay
  });

  // Function to close the pop-up by updating its state
  function closePopup() {
    showPopup = false;
  }
</script>

<main class="bg-white text-gray-800 font-sans">
  <!-- Hero Section -->
  <section
    class="relative h-[90vh] flex items-center justify-center bg-cover bg-center"
    style="background-image: url('/hero.jpg');"
    data-aos="fade"
  >
    <div class="absolute inset-0 bg-black/50 backdrop-blur-sm"></div>

    <div class="relative z-1 text-center px-6">
      <h1 class="text-4xl md:text-6xl font-extrabold text-white mb-4 drop-shadow-lg">
        Your Gateway to Travel - <span class="text-blue-200">SierraTravels</span>
      </h1>
      <p class="text-lg md:text-xl text-white font-medium mb-6 max-w-2xl mx-auto">
        Unforgettable journeys, dependable service, and travel comfort that feels like home.
      </p>
      <a
        href="#values"
        class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-full shadow-xl transition-transform duration-300 transform hover:scale-105"
      >
        Get Started
      </a>
    </div>
  </section>

  <!-- Our Values Section -->
  <section id="values" class="py-20 bg-gradient-to-br from-pink-200 to-pink-250" data-aos="fade-up">
    <div class="max-w-7xl mx-auto px-4 text-center">
      <h2 class="text-3xl font-extrabold mb-12 text-gray-800">Our Core Values</h2>
      <div class="grid gap-10 grid-cols-1 sm:grid-cols-2 md:grid-cols-3">
        <div
          class="bg-white p-6 rounded-3xl shadow-2xl hover:shadow-blue-200 transition-all duration-500 transform hover:-translate-y-1"
          data-aos="zoom-in"
          data-aos-delay="100"
        >
          <img src="reliability.jpg" alt="Reliability icon" class="w-20 h-20 mx-auto mb-4" />
          <h3 class="text-xl font-bold mb-2">Reliability</h3>
          <p class="font-medium">Count on us for consistent and timely travel solutions.</p>
        </div>

        <div
          class="bg-white p-6 rounded-3xl shadow-2xl hover:shadow-blue-100 transition-all duration-500 transform hover:-translate-y-1"
          data-aos="zoom-in"
          data-aos-delay="200"
        >
          <img src="comfort.jpg" alt="Comfort icon" class="w-20 h-20 mx-auto mb-4" />
          <h3 class="text-xl font-bold mb-2">Comfort</h3>
          <p class="font-medium">Every ride is tailored for relaxation and peace of mind.</p>
        </div>

        <div
          class="bg-white p-6 rounded-3xl shadow-2xl hover:shadow-blue-100 transition-all duration-500 transform hover:-translate-y-1"
          data-aos="zoom-in"
          data-aos-delay="300"
        >
          <img src="affordability.jpg" alt="Affordability icon" class="w-20 h-20 mx-auto mb-4" />
          <h3 class="text-xl font-bold mb-2">Affordability</h3>
          <p class="font-medium">Travel far without burning a hole in your wallet.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Know More Section as 2 Cards -->
  <section class="py-20 bg-white" data-aos="fade-up">
    <div class="max-w-6xl mx-auto px-4">
      <h2 class="text-3xl font-extrabold text-center mb-12">Know More About Us</h2>
      <div class="grid gap-8 md:grid-cols-2">
        <div
          class="bg-blue-50 p-8 rounded-3xl shadow-2xl hover:shadow-blue-100 transition-all duration-500 transform hover:-translate-y-1"
          data-aos="flip-left"
        >
          <h3 class="text-2xl font-bold mb-4 text-blue-700">What We Do</h3>
          <p class="text-gray-700 mb-4">
            SierraTravels provides top-notch employee transportation and reliable vehicle rentals across India.
            We specialize in comfort, punctuality, and professional service.
          </p>
          <a href="/contactus" class="text-blue-600 font-semibold hover:underline">Contact Us &rarr;</a>
        </div>

        <div
          class="bg-blue-50 p-8 rounded-3xl shadow-2xl hover:shadow-blue-100 transition-all duration-500 transform hover:-translate-y-1"
          data-aos="flip-right"
        >
          <h3 class="text-2xl font-bold mb-4 text-blue-700">Why Choose Us?</h3>
          <p class="text-gray-700 mb-4">
            Our well-maintained fleet, 24/7 support, and customer-first approach make us a trusted name for businesses and individuals alike.
          </p>
          <a href="/rentals" class="text-blue-600 font-semibold hover:underline">View Our Services &rarr;</a>
        </div>
      </div>
    </div>
  </section>

  <!-- Enquiry Section -->
<section
  id="enquiry"
  class="relative bg-cover bg-center py-24 px-6"
  style="background-image: url('https://source.unsplash.com/1600x900/?travel,bus,road');"
>
  <!-- Overlay -->
  <div class="absolute inset-0 bg-black bg-opacity-60"></div>

<div class="relative z-4 max-w-3xl mx-auto">
  <h2 class="text-3xl text-white font-extrabold text-center mb-4">Have a Doubt?</h2>
  <h2 class="text-2xl text-white font-bold text-center mb-12">Write us your question & we will get back to you</h2>

  <div class="backdrop-blur-lg bg-white/20 rounded-3xl p-8 shadow-2xl border border-white/30 text-white">
    <h2 class="text-3xl font-bold mb-6 text-center">Enquiry Form</h2>

    <!-- Begin mailto form -->
    <form
      action="mailto: mails@sierratravels.com"
      method="POST"
      enctype="text/plain"
      class="space-y-6"
    >
      <div>
        <label for="fullName" class="block mb-2 font-semibold">Full Name</label>
        <input
          id="fullName"
          type="text"
          name="Full Name"
          placeholder="Enter your name"
          class="w-full px-4 py-3 rounded-xl bg-white/80 text-black placeholder-gray-500 outline-none focus:ring-2 focus:ring-blue-400 transition"
          required
        />
      </div>

      <div>
        <label for="email" class="block mb-2 font-semibold">Email Address</label>
        <input
          id="email"
          type="email"
          name="Email"
          placeholder="Enter your email"
          class="w-full px-4 py-3 rounded-xl bg-white/80 text-black placeholder-gray-500 outline-none focus:ring-2 focus:ring-blue-400 transition"
          required
        />
      </div>

      <div>
        <label for="query" class="block mb-2 font-semibold">Query</label>
        <textarea
          id="query"
          name="Message"
          placeholder="Tell us what you need"
          rows="4"
          class="w-full px-4 py-3 rounded-xl bg-white/80 text-black placeholder-gray-500 outline-none focus:ring-2 focus:ring-blue-400 transition"
          required
        ></textarea>
      </div>

      <div class="text-center">
        <button
          type="submit"
          class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-full shadow-lg transition duration-300"
        >
          Submit Enquiry
        </button>
      </div>
    </form>
    <!-- End mailto form -->
  </div>
</div>

</section>

<section class="bg-white py-16 px-6 md:px-12">
  <div class="max-w-7xl mx-auto">
    <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-6 text-center">Security</h2>
    <p class="text-center text-gray-600 max-w-2xl mx-auto mb-12">
      We prioritize your safety with a comprehensive approach combining technology, compliance, and care.
    </p>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition">
        <h3 class="font-semibold text-blue-600">GPS with Live Tracking</h3>
        <p class="text-sm text-gray-600 mt-2">Monitor real-time location of vehicles for enhanced security and visibility.</p>
      </div>

      <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition">
        <h3 class="font-semibold text-blue-600">Safety Belts for Passengers</h3>
        <p class="text-sm text-gray-600 mt-2">All seats equipped with seat belts to ensure passenger safety.</p>
      </div>

      <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition">
        <h3 class="font-semibold text-blue-600">Driver & Vehicle Compliance</h3>
        <p class="text-sm text-gray-600 mt-2">Both software-based and manual checks ensure legal and safety compliance.</p>
      </div>

      <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition">
        <h3 class="font-semibold text-blue-600">Regular Maintenance</h3>
        <p class="text-sm text-gray-600 mt-2">Vehicles undergo routine servicing to avoid breakdowns and ensure performance.</p>
      </div>

      <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition">
        <h3 class="font-semibold text-blue-600">Driver Document Renewals</h3>
        <p class="text-sm text-gray-600 mt-2">On-time renewal tracking for licenses and permits for uninterrupted service.</p>
      </div>

      <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition">
        <h3 class="font-semibold text-blue-600">Cleanliness Checks</h3>
        <p class="text-sm text-gray-600 mt-2">Vehicles are inspected regularly to maintain hygiene and comfort.</p>
      </div>

      <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition col-span-1 sm:col-span-2 lg:col-span-3">
        <h3 class="font-semibold text-blue-600">Safety Kits & Emergency Readiness</h3>
        <p class="text-sm text-gray-600 mt-2">
          Each vehicle is equipped with First Aid, Fire Extinguishers, Do & Don’ts instructions, and emergency contacts.
        </p>
      </div>
    </div>
  </div>
</section>


</main>

<!-- Pop-up Modal -->
<!-- This conditional block now renders a non-blocking toast notification -->
{#if showPopup}
  <div
    class="fixed bottom-4 left-4 z-50 p-4"
    transition:fly={{ y: 50, duration: 500 }}
  >
    <div
      class="bg-gradient-to-r from-blue-500 to-blue-600 text-white rounded-lg shadow-2xl p-4 max-w-sm w-11/12 flex items-center justify-between transform transition-transform duration-200 hover:scale-[1.02]"
    >
      <!-- Icon and Text Container -->
      <div class="flex items-center space-x-3">
        <!-- Success Checkmark Icon (Inline SVG for simplicity) -->
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-white flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
        </svg>

        <div>
          <h3 class="text-lg font-bold mb-1">WE updated our name!</h3>
          <p class="text-sm">We are now "<span class="font-semibold">SierraTravels!</span>".</p>
        </div>
      </div>

      <!-- Dismiss Button -->
      <button
        on:click={closePopup}
        class="text-white hover:text-gray-200 transition-colors"
        aria-label="Dismiss notification"
      >
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>
  </div>
{/if}
