
<script lang="ts">
  import { onMount } from 'svelte';

  const logos: string[] = [
    "/zerodha.png",
    "/medusind.png",
    "/brightdrive.jpg",
    "/ahcs.jpg"
  ];

  let scrollContainer: HTMLElement;

  // Auto scroll logic
  onMount(() => {
    const scrollSpeed = 1; // Adjust speed here
    let frame: number;

    function autoScroll() {
      if (scrollContainer) {
        scrollContainer.scrollLeft += scrollSpeed;
        // Reset to start when reaching the end
        // A small buffer is added to handle potential floating point inaccuracies
        if (
          scrollContainer.scrollLeft >=
          scrollContainer.scrollWidth - scrollContainer.clientWidth - 1
        ) {
          scrollContainer.scrollLeft = 0;
        }
      }
      frame = requestAnimationFrame(autoScroll);
    }

    frame = requestAnimationFrame(autoScroll);

    return () => cancelAnimationFrame(frame); // cleanup
  });
</script>
<section
  class="bg-white py-16 px-4 md:px-10 lg:px-20"
  data-aos="fade-up"
>
  <!-- Heading -->
  <div class="text-center mb-12" data-aos="fade-down">
    <h1 class="text-4xl md:text-5xl font-extrabold text-gray-800 mb-4 tracking-tight">
      About <span class="text-blue-600">Sri Annapoorneshwari Travels</span>
    </h1>
    <p class="text-lg font-semibold max-w-3xl mx-auto leading-relaxed" data-aos="fade-up" data-aos-delay="200">
      At Annapoorneshwari Travels, we do more than move people — we craft memorable and safe journeys powered by comfort, reliability, and heart.
    </p>
  </div>

  <div
  class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-1 gap-8 bg-gradient-to-br from-blue-100 to-blue-200 rounded-3xl shadow-2xl p-8"
  data-aos="fade-up"
>
  <!-- Text Section -->
  <div class="space-y-5" data-aos="fade-right" data-aos-delay="200">
    <h2 class="flex items-center text-blue-800">
  <img src="logobg.png" alt="Sri Annapoorneshwari Travels Logo" class="h-30 sm:h-50 w-auto mr-3">
  <span class="text-xl sm:text-3xl font-extrabold">
    Sri Annapoorneshwari Travels
  </span>
</h2>



    <p class="text-justify text-base md:text-lg leading-relaxed text-gray-800">
      <strong>Sri Annapoorneshwari Travels</strong> was founded in 1991 by Mr. Nagesh, with a simple vision — to provide reliable and trustworthy travel services. Over three decades of commitment have led to steady growth, adapting to evolving needs and expanding our reach.
    </p>
    <p class="text-justify text-base md:text-lg leading-relaxed text-gray-800">
     Today, it is jointly managed by Mr. Nagesh and Mr. Shreyas — a team blending experience with innovation to deliver seamless travel solutions across various sectors.
    </p>
    <p class="text-justify text-base md:text-lg leading-relaxed text-gray-800">
      Built on a foundation of trust, punctuality, and customer satisfaction, Annapoorneshwari Travels continues to move forward — one journey at a time.
    </p>
    <p class="text-justify text-base md:text-lg leading-relaxed text-gray-800">
      Based in Bangalore, Annapoorneshwari Travels is a full-stack corporate car rental services company offering a wide range of vehicles tailored to your needs. Our mission is to deliver safe, reliable, and affordable transport services with unmatched customer service and quality.
    </p>
    <ul class="space-y-2 text-gray-800 pt-2">
      <li class="flex items-start">
        <span class="bg-green-200 text-green-800 rounded-full p-2 mr-3 shadow">✓</span>
        Employee Transportation
      </li>
      <li class="flex items-start">
        <span class="bg-green-200 text-green-800 rounded-full p-2 mr-3 shadow">✓</span>
        Ad-hoc Cabs & Airport Transfers
      </li>
      <li class="flex items-start">
        <span class="bg-green-200 text-green-800 rounded-full p-2 mr-3 shadow">✓</span>
        Corporate & Local Travel Packages
      </li>
      <li class="flex items-start">
        <span class="bg-green-200 text-green-800 rounded-full p-2 mr-3 shadow">✓</span>
        Event & Outstation Travel
      </li>
      <li class="flex items-start">
        <span class="bg-green-200 text-green-800 rounded-full p-2 mr-3 shadow">✓</span>
        Buses on Rent
      </li>
    </ul>
  </div>

</div>
<!-- Image Section -->
  <!-- <div
    class="relative overflow-hidden rounded-3xl shadow-xl"
    data-aos="zoom-in"
    data-aos-delay="500"
  >
    <img
      src="/logo.jpg"
      alt="Annapoorneshwari Travels Logo"
      class="w-full h-full object-cover hover:scale-105 transition-transform duration-500 ease-in-out"
    />
  </div> -->

</section>


<!-- Carousel clintele -->
<section class="bg-black py-12 px-4">
  <div class="max-w-7xl mx-auto">
    <h2 class="text-white text-3xl font-bold mb-6">Our Clintele</h2>

    <div
      class="overflow-x-auto whitespace-nowrap hide-scrollbar"
      bind:this={scrollContainer}
    >
      <div class="flex space-x-6">
        {#each logos as logo}
          <div class="min-w-[200px] h-[120px] flex items-center justify-center bg-white rounded-lg shadow-md flex-shrink-0 hover:scale-105 transition-transform duration-300">
            <img src={logo} alt="Client Logo" class="max-h-[80px] max-w-[160px] object-contain" />
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>

<section
  class="bg-white py-20 px-6 md:px-12"
  data-aos="fade-up"
>
  <div class="max-w-7xl mx-auto">
    <!-- Mission & Vision -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12 mb-20">
      <div
        class="bg-gradient-to-br from-pink-150 to-pink-200 rounded-xl p-8 shadow hover:shadow-md transition duration-300"
        data-aos="fade-right"
        data-aos-delay="200"
      >
        <h2 class="text-2xl font-bold text-blue-700 mb-3">Our Mission</h2>
        <p class="font-medium leading-relaxed">
          To provide reliable, safe, and efficient
          transportation solutions that exceed
          customer expectations and to deliver
          on-time services with a commitment
          to quality and reliability.
        </p>
      </div>
      <div
        class="bg-gradient-to-br from-pink-150 to-pink-200 rounded-xl p-8 shadow hover:shadow-md transition duration-300"
        data-aos="fade-left"
        data-aos-delay="400"
      >
        <h2 class="text-2xl font-bold text-blue-600 mb-3">Our Vision</h2>
        <p class="font-medium leading-relaxed">
          To be recognised as a leader in the
          transport industry, setting benchmarks
          for service excellence, innovation & meet
          the evolving needs of our clients with
          customised & flexible transportation
          solutions.
        </p>
      </div>
    </div>

    <!-- Strengths -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      {#each [
        { title: 'Safety First', text: 'Strict protocols, GPS tracking, and regular maintenance to ensure your safety.' },
        { title: 'Customer-Centric', text: 'We listen closely and deliver travel solutions with empathy and precision.' },
        { title: 'Experienced Staff', text: 'From courteous drivers to responsive support—our team is our strength.' }
      ] as item, i}
        <div
          class="bg-white border border-gray-200 rounded-xl p-6 shadow hover:shadow-md transition duration-300"
          data-aos="fade-up"
          data-aos-delay={i * 300}
        >
          <h3 class="text-lg font-bold text-blue-600 mb-2">{item.title}</h3>
          <p class="font-medium text-sm leading-relaxed">{item.text}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .hide-scrollbar::-webkit-scrollbar {
    display: none;
  }
  .hide-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
</style>