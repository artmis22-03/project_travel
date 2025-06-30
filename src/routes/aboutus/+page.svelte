<script>
  const team = [
    {
      name: "Nagesh G",
      title: "Founder",
      image: "/founder.jpg", // replace with actual image URL
    },
    {
      name: "Shreyas W N",
      title: "Managing Director",
      image: "/md.jpg", // replace with actual image URL
    },
  ];
</script>
<section
  class="bg-white py-16 px-4 md:px-10 lg:px-20"
  data-aos="fade-up"
>
  <!-- Heading -->
  <div class="text-center mb-12" data-aos="fade-down">
    <h1 class="text-4xl md:text-5xl font-extrabold text-gray-800 mb-4 tracking-tight">
      About <span class="text-blue-600">SierraTravels</span>
    </h1>
    <p class="text-lg font-semibold max-w-3xl mx-auto leading-relaxed" data-aos="fade-up" data-aos-delay="200">
      At SierraTravels, we do more than move people — we craft memorable and safe journeys powered by comfort, reliability, and heart.
    </p>
  </div>

  <div
    class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-8 bg-gradient-to-br from-blue-150 to-blue-200 rounded-3xl shadow-2xl p-8"
    data-aos="zoom-in-up"
  >
    <!-- Text -->
    <div class="space-y-5" data-aos="fade-right" data-aos-delay="300">
      <h2 class="text-3xl font-extrabold text-blue-800">SierraTravels</h2>
      <p class="font-medium text-justify text-base md:text-lg leading-relaxed">
        SIERRA TRAVELS is part of the Group’s overarching vision to become a world-class transport solution company...
      </p>
      <ul class="space-y-3 text-gray-800">
        <li class="flex items-center">
          <span class="bg-green-200 text-green-800 rounded-full p-2 mr-3 shadow">✓</span>
          State and interstate coverage
        </li>
        <li class="flex items-center">
          <span class="bg-green-200 text-green-800 rounded-full p-2 mr-3 shadow">✓</span>
          Wide range of vehicles
        </li>
        <li class="flex items-center">
          <span class="bg-green-200 text-green-800 rounded-full p-2 mr-3 shadow">✓</span>
          24/7 customer support
        </li>
      </ul>
    </div>

    <!-- Image -->
    <div
      class="relative overflow-hidden rounded-3xl shadow-xl"
      data-aos="zoom-in"
      data-aos-delay="600"
    >
      <img
        src="/logo.jpg"
        alt="Rental travel"
        class="w-full h-full object-cover hover:scale-105 transition-transform duration-500 ease-in-out"
      />
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
          To provide reliable, safe, and efficient...
        </p>
      </div>
      <div
        class="bg-gradient-to-br from-pink-150 to-pink-200 rounded-xl p-8 shadow hover:shadow-md transition duration-300"
        data-aos="fade-left"
        data-aos-delay="400"
      >
        <h2 class="text-2xl font-bold text-blue-600 mb-3">Our Vision</h2>
        <p class="font-medium leading-relaxed">
          To be recognised as a leader in the...
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

<section
  class="bg-gradient-to-br from-gray-100 to-white py-20 px-4 md:px-10 lg:px-20"
  data-aos="fade-up"
>
  <div class="max-w-6xl mx-auto text-center">
    <h2 class="text-4xl md:text-5xl font-extrabold text-gray-800 mb-16" data-aos="fade-down">Meet Our Leadership</h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-12 place-items-center">
      {#each team as member, i}
        <div
          class="bg-white p-6 rounded-2xl shadow-md hover:shadow-2xl hover:scale-[1.03] transform transition-all duration-300 w-72"
          data-aos="zoom-in"
          data-aos-delay={i * 200}
        >
          <img
            src={member.image}
            alt={member.name}
            class="w-32 h-32 mx-auto rounded-full object-cover mb-6 border-4 border-blue-100 shadow-md"
          />
          <h3 class="text-2xl font-semibold text-gray-800">{member.name}</h3>
          <p class="text-gray-600 mt-1 text-sm">{member.title}</p>
        </div>
      {/each}
    </div>
  </div>
</section>
