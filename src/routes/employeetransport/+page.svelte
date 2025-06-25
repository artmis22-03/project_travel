<script>
  const services = [
    {
      title: "Employee Shuttle Services",
      description:
        "Our employee shuttle services provide convenient and reliable transportation options for companies, ensuring smooth and punctual commuting for their workforce.",
      image: "/etios.jpg",
      reverse: false,
    },
    {
      title: "Executive Transportation",
      description:
        "Our executive transportation services cater to the specific needs of high-level professionals, providing luxurious vehicles and professional chauffeurs for a comfortable and prestigious travel experience.",
      image: "/hycross.jpg",
      reverse: true,
    },
    {
      title: "Corporate Pickup and Drop Solutions",
      description:
        "We offer tailored pickup and drop solutions for corporate clients, streamlining the transportation process and ensuring prompt and efficient travel for executives and employees.",
      image: "/crysta.jpg",
      reverse: false,
    },
    {
      title: "Ad-Hoc Cabs",
      description:
        "On-demand cab services for employees, used for urgent or unscheduled travel. Typically used for client meetings, hospital visits, or unplanned office travel needs.",
      image: "/urbania.jpg",
      reverse: true,
    },
    {
      title: "Airport Transfer",
      description:
        "Pre-arranged transport for employees traveling for business, ensuring smooth and timely transfer between the airport and office or home, including assistance for early morning or late-night flights.",
      image: "/etios.jpg",
      reverse: false,
    },
    {
      title: "Event Travel",
      description:
        "Transport arrangements for company events such as team outings, conferences, or training sessions. This could involve multiple pick-up points and coordinating large fleets of buses or vans.",
      image: "/urbania.jpg",
      reverse: true,
    },
  ];
</script>

<!-- Hero Section -->
<section
  class="relative h-[80vh] flex items-center justify-center bg-cover bg-center"
  style="background-image: url('/ser2.jpg');"
>
  <div class="absolute inset-0 bg-black/60 backdrop-blur-sm"></div>
  <div class="relative z-1 text-center text-white px-4">
    <h1 class="text-4xl md:text-5xl font-bold mb-4 drop-shadow">Reliable Employee Transport Services</h1>
    <p class="text-lg md:text-xl max-w-2xl mx-auto mb-6 drop-shadow">
      Flexible and professional transport solutions for businesses and executives.
    </p>
    <a
      href="/contactus"
      class="inline-block bg-blue-600 hover:bg-blue-700 transition text-white font-semibold py-3 px-6 rounded-lg shadow-lg"
    >
      Get a Quote
    </a>
  </div>
</section>

<!-- Introduction -->
<section class="bg-gray-50 py-16">
  <div class="max-w-4xl mx-auto px-6 text-center">
    <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">Tailored Employee transport Solutions</h2>
    <p class="text-gray-600 text-md md:text-lg">
      Whether it’s daily employee commutes, executive transfers, or flexible corporate pickups, our fleet and professional drivers ensure comfort, safety, and punctuality across all services.
    </p>
  </div>
</section>

<!-- Services Section -->
<section class="bg-white py-16">
  <div class="space-y-24">
    {#each services as service}
      <div class={`flex flex-col md:flex-row items-center gap-10 px-6 max-w-7xl mx-auto ${service.reverse ? 'md:flex-row-reverse' : ''}`}>
        <img
          src={service.image}
          alt={service.title}
          class="w-full md:w-1/2 h-72 object-cover rounded-2xl shadow-lg hover:scale-105 transition duration-300"
        />
        <div class="md:w-1/2">
          <h3 class="text-2xl md:text-3xl font-extrabold text-blue-900 mb-4">{service.title}</h3>
          <p class="text-gray-700 text-md md:text-lg leading-relaxed">{service.description}</p>
        </div>
      </div>
    {/each}
  </div>
</section>

<!-- CTA Section -->
<section class="bg-blue-50 py-20">
  <div class="text-center max-w-3xl mx-auto px-4">
    <h2 class="text-3xl font-bold text-blue-800 mb-4">Ready to Book a Ride?</h2>
    <p class="text-gray-700 mb-6">
      Connect with us to plan your next transport requirement. We're committed to professional service and competitive pricing.
    </p>
    <a
      href="/contactus"
      class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-medium py-3 px-6 rounded-lg shadow transition"
    >
      Contact Us
    </a>
  </div>
</section>
