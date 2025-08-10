<script>
  const services = [
    {
      title: "Employee Transportation Services",
      description:
        "Sri Annapoorneshwari Travels is a trusted provider of employee transportation services, committed to delivering safe, efficient, and convenient travel solutions for your workforce. With years of experience in the transportation industry, we cater to companies of all sizes, ensuring seamless commutes for their workforce while maintaining high standards of safety, punctuality, and customer service.",
      image: "/emptransport.jpg",
      reverse: false,
    },
    {
      title: "Airport Transfer",
      description:
        "Pickup and drop services to and from airports, ensuring timely and comfortable travel for employees, guests, or executives.",
      image: "/airpost.jpg",
      reverse: true,
    },
    {
      title: "Ad-Hoc Cabs",
      description:
        "On-demand cab services for employees or executives that are not part of a fixed route or schedule. Useful for last-minute meetings, urgent trips, or visitor transport.",
      image: "/adhoc.jpg",
      reverse: false,
    },
    {
      title: "Corporate Travel",
      description:"Customized travel solutions for company executives or teams for business meetings, conferences, and official visits—includes planning, transport, and coordination.",
      image: "/corporate.jpg",
      reverse: true,
    },
    {
      title: "Local Packages",
      description:"Hourly or full-day cab/bus rental options for intra-city travel, suitable for client visits, city tours for guests, or team travel.",
      image: "/localpackage.jpg",
      reverse: false,
    },           
    {
      title: "Event Travel",
      description:"Transportation for corporate events, team outings, conferences, or company celebrations. Includes group logistics planning and vehicle deployment.",
      image: "/eventtravel.jpg",
      reverse: true,
    },
    {
      title: "Buses On Rent",
      description:"Fleet of buses available for short- or long-term rental, suitable for bulk employee movement, events, excursions, or training programs.",
      image: "/bus.jpg",
      reverse: false,
    },
    {
      title: "Outstation Travel",
      description:"Transport services for trips outside the city—whether for official site visits, inter-city meetings, or team excursions. Available as one-way or round trip.",
      image: "/outstation.jpg",
      reverse: true,
    },
  ];
</script>

<!-- Hero Section -->
<!-- Hero Section -->
<section
  class="relative h-[80vh] flex items-center justify-center bg-cover bg-center"
  style="background-image: url('/ser2.jpg');"
  data-aos="fade"
>
  <div class="absolute inset-0 bg-black/60 backdrop-blur-sm"></div>
  <div class="relative z-1 text-center text-white px-4" data-aos="zoom-in">
    <h1 class="text-4xl md:text-5xl font-bold mb-4 drop-shadow">Our Services</h1>
    <p class="text-lg md:text-xl max-w-2xl mx-auto mb-6 drop-shadow">
      Where Reliability Meets Quality
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
<section class="bg-gray-50 py-16" data-aos="fade-up">
  <div class="max-w-4xl mx-auto px-6 text-center">
    <h2 class="text-3xl md:text-4xl font-bold mb-4">Tailored Transport Solutions</h2>
    <p class="font-medium text-md md:text-lg">
      At Annaporneshwari Travels, we ensure every journey is marked by comfort, safety, and reliability, tailored to whether it’s daily commutes, special trips, or custom travel solutions. Know more about our Services below:
    </p>
  </div>
</section>

<!-- Services Section -->
<section class="bg-white py-16">
  <div class="space-y-24">
    {#each services as service, i}
      <div
        class={`flex flex-col md:flex-row items-center gap-10 px-6 max-w-7xl mx-auto ${service.reverse ? 'md:flex-row-reverse' : ''}`}
        data-aos="fade-up"
        data-aos-delay={i * 200}
      >
        <img
          src={service.image}
          alt={service.title}
          class="w-full md:w-1/2 h-72 object-cover rounded-2xl shadow-lg hover:scale-105 transition duration-300"
          data-aos="zoom-in"
          data-aos-delay={i * 200 + 100}
        />
        <div class="md:w-1/2" data-aos="fade-left" data-aos-delay={i * 200 + 200}>
          <h3 class="text-2xl md:text-3xl font-extrabold text-blue-900 mb-4">{service.title}</h3>
          <p class="font-medium text-md md:text-lg leading-relaxed">{service.description}</p>
        </div>
      </div>
    {/each}
  </div>
</section>

<!-- CTA Section -->
<section class="bg-blue-50 py-20" data-aos="fade-up">
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

