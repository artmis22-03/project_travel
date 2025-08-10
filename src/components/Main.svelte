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
    style="background-image: url('/main.jpg');"
    data-aos="fade"
  >
    <div class="absolute inset-0 bg-black/50 backdrop-blur-none"></div>

    <div class="relative z-1 text-center px-6">
      <h1 class="text-4xl md:text-6xl font-extrabold text-white mb-4 drop-shadow-lg">
        Your Gateway to Travel - <span class="text-blue-200">Sri Annapoorneshwari Travels</span>
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
  <section id="values" class="py-20 bg-gradient-to-br from-purple-200 to-purple-250" data-aos="fade-up">
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
<section class="bg-black text-white py-16">
  <div class="max-w-6xl mx-auto px-6">
    <h2 class="text-purple-400 uppercase tracking-widest mb-4">Testimonials</h2>
    <h3 class="text-4xl font-bold text-purple-200 mb-12">
      What Our Clients Say
    </h3>

    <div class="grid md:grid-cols-2 gap-8">
      <!-- Testimonial Card 1 -->
      <div class="bg-[#0b0f1a] rounded-xl p-6 shadow-lg hover:shadow-purple-500/20 transition">
        <p class="text-gray-300 mb-6">
          Sri Annapoorneshwari Travels has always provided great support for BrightDrive.
          Your operations team is excellent on-site and consistently meets our day-to-day needs.
          Whether it’s additional support for new vehicles, events, late-night cabs, or luxury buses for clients,
          you’ve always been supportive.
        </p>
        <p class="font-semibold text-purple-300">ESWAR D</p>
        <p class="text-gray-500 text-sm">Bright DriveHCS Bangalore</p>
      </div>

      <!-- Testimonial Card 2 -->
      <div class="bg-[#0b0f1a] rounded-xl p-6 shadow-lg hover:shadow-purple-500/20 transition">
        <p class="text-gray-300 mb-6">
          Their live tracking feature and well-maintained vehicles give us complete peace of mind
          for our daily corporate travel needs.
        </p>
        <p class="font-semibold text-purple-300">Priya Sharma</p>
        <p class="text-gray-500 text-sm">HR Head</p>
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
          data-aos="flip-left">
          <h3 class="text-2xl font-bold mb-4 text-blue-700">What We Do</h3>
          <p class="text-gray-700 mb-4">
            Annapoorneshwari Travels provides top-notch employee transportation and reliable vehicle rentals across India.
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
          <a href="/employeetransport" class="text-blue-600 font-semibold hover:underline">View Our Services &rarr;</a>
        </div>
      </div>
    </div>
  </section>

<section class="bg-black text-white py-16 px-6 md:px-12" data-aos="fade-up">
  <div class="max-w-7xl mx-auto grid md:grid-cols-2 gap-12 items-center">
    
    <!-- Left Column -->
    <div class="space-y-6">
      <p class="uppercase tracking-widest text-purple-400 text-sm">About Us</p>
      <h2 class="text-4xl md:text-5xl font-extrabold text-purple-200 leading-tight">
        Reliable Corporate Travel, <br />
        Backed by Decades of Experience
      </h2>
      <p class="text-gray-300 text-lg leading-relaxed">
        Founded in 1991, we’ve built a reputation for punctuality, professionalism, and premium service.
        Today, Sri Annapoorneshwari Travels stands as a trusted provider of full-stack corporate car rental services.
      </p>
      <a
  href="/aboutus"
  class="mt-4 inline-block bg-purple-600 hover:bg-purple-700 text-white font-semibold px-6 py-3 rounded-full transition duration-300"
>
  Know More &rarr;
</a>

    </div>

    <!-- Right Column: Stats Grid -->
    <div class="grid grid-cols-2 gap-6">
      <div class="bg-gray-900 p-6 rounded-2xl text-center shadow-lg" data-aos="zoom-in" data-aos-delay="100">
        <p class="text-4xl font-bold text-purple-400">30+</p>
        <p class="mt-2 text-gray-400">Years of Experience</p>
      </div>
      <div class="bg-gray-900 p-6 rounded-2xl text-center shadow-lg" data-aos="zoom-in" data-aos-delay="200">
        <p class="text-4xl font-bold text-purple-400">200+</p>
        <p class="mt-2 text-gray-400">Corporate Clients</p>
      </div>
      <div class="bg-gray-900 p-6 rounded-2xl text-center shadow-lg" data-aos="zoom-in" data-aos-delay="300">
        <p class="text-4xl font-bold text-purple-400">100+</p>
        <p class="mt-2 text-gray-400">Daily Trips</p>
      </div>
      <div class="bg-gray-900 p-6 rounded-2xl text-center shadow-lg" data-aos="zoom-in" data-aos-delay="400">
        <p class="text-4xl font-bold text-purple-400">1M+</p>
        <p class="mt-2 text-gray-400">Trips Completed</p>
      </div>
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
      <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition flex items-start space-x-3">
        <img src="gps.png" alt="GPS Icon" class="w-6 h-6 mt-1">
        <div>
          <h3 class="font-semibold text-blue-600">GPS with Live Tracking</h3>
          <p class="text-sm text-gray-600 mt-2">
            Monitor real-time location of vehicles for enhanced security and visibility.
          </p>
        </div>
    </div>
    <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition flex items-start space-x-3">
        <img src="safetybelt.png" alt="GPS Icon" class="w-6 h-6 mt-1">
        <div>
          <h3 class="font-semibold text-blue-600">Safety Belts for Passengers</h3>
          <p class="text-sm text-gray-600 mt-2">
            All seats equipped with seat belts to ensure passenger safety.
          </p>
        </div>
    </div>
    <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition flex items-start space-x-3">
        <img src="compliance.png" alt="GPS Icon" class="w-6 h-6 mt-1">
        <div>
          <h3 class="font-semibold text-blue-600">Driver & Vehicle Compliance</h3>
          <p class="text-sm text-gray-600 mt-2">
            Both software-based and manual checks ensure legal and safety compliance.
          </p>
        </div>
    </div>
    <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition flex items-start space-x-3">
        <img src="maintanence.png" alt="GPS Icon" class="w-6 h-6 mt-1">
        <div>
          <h3 class="font-semibold text-blue-600">Regular Maintenance</h3>
          <p class="text-sm text-gray-600 mt-2">
            Vehicles undergo routine servicing to avoid breakdowns and ensure performance.
          </p>
        </div>
    </div>
    <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition flex items-start space-x-3">
        <img src="safetykit.png" alt="GPS Icon" class="w-6 h-6 mt-1">
        <div>
          <h3 class="font-semibold text-blue-600">Safety Kits & Emergency Readiness</h3>
          <p class="text-sm text-gray-600 mt-2">
            Each vehicle is equipped with First Aid, Fire Extinguishers, Do & Don’ts instructions, and emergency contacts.
          </p>
        </div>
    </div>
    <div class="bg-gray-50 p-6 rounded-lg shadow hover:shadow-md transition flex items-start space-x-3">
        <img src="cleanliness.png" alt="GPS Icon" class="w-6 h-6 mt-1">
        <div>
          <h3 class="font-semibold text-blue-600">Cleanliness Checks</h3>
          <p class="text-sm text-gray-600 mt-2">
            Vehicles are inspected regularly to maintain hygiene and comfort.
          </p>
        </div>
    </div>
    </div>
  </div>
</section>


</main>

<!-- Pop-up Modal -->
<!-- This conditional block now renders a non-blocking toast notification -->
{#if showPopup}
  <div
    class="fixed bottom-6 left-6 z-50"
    transition:fly={{ y: 50, duration: 600 }}
  >
    <div
      class="relative bg-gradient-to-r from-orange-400 via-pink-400 to-purple-500 text-white rounded-2xl shadow-xl p-6 w-[90vw] max-w-sm animate-slide-in overflow-hidden"
    >
      <!-- Decorative Clouds -->
      <div class="absolute top-0 left-0 w-full h-full opacity-20 pointer-events-none">
        <svg viewBox="0 0 200 100" class="w-full h-full">
          <ellipse cx="50" cy="50" rx="50" ry="25" fill="white" />
          <ellipse cx="150" cy="50" rx="50" ry="25" fill="white" />
        </svg>
      </div>

      <!-- Airplane Icon -->
      

      <!-- Highlighted Name -->
      <p class="text-sm relative z-10">
        Say hello to  
        <span class="block text-2xl font-extrabold text-blue-600 drop-shadow-lg">
          Sri Annapoorneshwari Travels
        </span>  
        — your commute partner!
      </p>

      <!-- Button -->
      <button
        on:click={closePopup}
        class="mt-4 bg-white text-orange-600 font-bold px-5 py-1.5 rounded-full shadow hover:scale-105 transition relative z-10"
      >
        Let’s Go!
      </button>
    </div>
  </div>
{/if}

<style>
  @keyframes slide-in {
    0% { transform: translateY(50px) scale(0.95); opacity: 0; }
    60% { transform: translateY(0) scale(1.05); opacity: 1; }
    100% { transform: scale(1); }
  }
  .animate-slide-in {
    animation: slide-in 0.6s ease-out;
  }

  @keyframes plane {
    0% { transform: translateX(0) rotate(0deg); }
    50% { transform: translateX(5px) rotate(2deg); }
    100% { transform: translateX(0) rotate(0deg); }
  }
  .animate-plane {
    animation: plane 1.5s ease-in-out infinite;
  }
</style>
