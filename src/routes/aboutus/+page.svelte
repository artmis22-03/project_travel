<script>
  const team = [
    {
      name: "Name",
      title: "Founder",
      image: "/founder.jpg", // replace with actual image URL
    },
    {
      name: "Name",
      title: "Managing Director",
      image: "/md.jpg", // replace with actual image URL
    },
  ];
</script>
<section class="bg-white py-16 px-4 md:px-10 lg:px-20">
  <!-- Heading -->
    <div class="text-center mb-12">
      <h1 class="text-4xl md:text-5xl font-extrabold text-gray-800 mb-4 tracking-tight">About <span class="text-blue-600">SierraTravels</span></h1>
      <p class="text-lg text-gray-600 max-w-3xl mx-auto leading-relaxed">
        At SierraTravels, we do more than move people—we craft memorable and safe journeys powered by comfort, reliability, and heart.
      </p>
    </div>
  <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-10 items-center">
    
    <!-- Text Content -->
    <div>
      <h2 class="text-2xl font-extrabold text-gray-800 mb-4">SierraTravels </h2>
      <p class="text-gray-600 text-lg mb-6 leading-relaxed">
        The company is named as SIERRA TRAVELS as part of the
        Group’s overarching vision to become a world class transport solution company.
        Committed to its mission of delivering customer satisfaction  &
        is a pioneer of new services, design and technology and the
        leader that sets industry Standards. SIERRA also has business
        interests in Air, Car, Local & Airport Transport
      </p>
      <ul class="space-y-2 text-gray-700">
        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> State and interstate coverage</li>
        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Wide range of vehicles</li>
        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> 24/7 customer support</li>
      </ul>
    </div>

    <!-- Image -->
    <div class="relative overflow-hidden rounded-2xl shadow-blue-50-lg">
      <img 
        src="/logo.jpg" 
        alt="Rental travel" 
        class="w-full h-full object-cover hover:scale-105 transition-transform duration-300"
      />
    </div>

  </div>
</section>

<section class="bg-white py-20 px-6 md:px-12 transition-all duration-500">
  <div class="max-w-7xl mx-auto">
    
    
    <!-- Mission & Vision -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12 mb-20">
      <div class="bg-gray-50 rounded-xl p-8 shadow-sm hover:shadow-md transition duration-300">
        <h2 class="text-2xl font-semibold text-blue-600 mb-3">Our Mission</h2>
        <p class="text-gray-700 leading-relaxed">
          To provide reliable, safe, and efficient
          customer expectations and to deliver
          on-time services with a commitment
          to quality and reliability
          transportation solutions that exceed
        </p>
      </div>
      <div class="bg-gray-50 rounded-xl p-8 shadow-sm hover:shadow-md transition duration-300">
        <h2 class="text-2xl font-semibold text-blue-600 mb-3">Our Vision</h2>
        <p class="text-gray-700 leading-relaxed">
           To be recognised as a leader in the
           for service excellence, innovation & meet
           the evolving needs of our clients with
           customised & flexible transportation
           solutions transport industry, setting benchmarks
        </p>
      </div>
    </div>

    <!-- Strengths or Values -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      {#each [
        { title: 'Safety First', text: 'Strict protocols, GPS tracking, and regular maintenance to ensure your safety.' },
        { title: 'Customer-Centric', text: 'We listen closely and deliver travel solutions with empathy and precision.' },
        { title: 'Experienced Staff', text: 'From courteous drivers to responsive support—our team is our strength.' }
      ] as item}
        <div class="bg-white border border-gray-200 rounded-xl p-6 shadow hover:shadow-md transition duration-300">
          <h3 class="text-lg font-semibold text-blue-600 mb-2">{item.title}</h3>
          <p class="text-gray-600 text-sm leading-relaxed">{item.text}</p>
        </div>
      {/each}
    </div>

    <!-- Optional Image or CTA -->
    <!-- <div class="mt-20 text-center">
      <img
        src="/images/about-banner.jpg"
        alt="Fleet or Team"
        class="mx-auto rounded-xl shadow-md w-full md:w-3/4 transition duration-300 hover:shadow-xl"
      />
      <p class="text-sm text-gray-500 mt-3">Delivering exceptional service across every mile.</p>
    </div> -->
  </div>
</section>
<section class="bg-gradient-to-br from-gray-100 to-white py-20 px-4 md:px-10 lg:px-20">
  <div class="max-w-6xl mx-auto text-center">
    <h2 class="text-4xl md:text-5xl font-extrabold text-gray-800 mb-16">Meet Our Leadership</h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-12 place-items-center">
      {#each team as member}
        <div class="bg-white p-6 rounded-2xl shadow-md hover:shadow-2xl hover:scale-[1.03] transform transition-all duration-300 w-72">
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

