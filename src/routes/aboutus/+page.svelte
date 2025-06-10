<section class="bg-white py-20 px-6 md:px-12 transition-all duration-500">
  <div class="max-w-7xl mx-auto">
    <!-- Heading -->
    <div class="text-center mb-12">
      <h1 class="text-4xl md:text-5xl font-extrabold text-gray-800 mb-4 tracking-tight">About <span class="text-blue-600">SierraTravels</span></h1>
      <p class="text-lg text-gray-600 max-w-3xl mx-auto leading-relaxed">
        At SierraTravels, we do more than move people—we craft memorable and safe journeys powered by comfort, reliability, and heart.
      </p>
    </div>

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
    <div class="mt-20 text-center">
      <img
        src="/images/about-banner.jpg"
        alt="Fleet or Team"
        class="mx-auto rounded-xl shadow-md w-full md:w-3/4 transition duration-300 hover:shadow-xl"
      />
      <p class="text-sm text-gray-500 mt-3">Delivering exceptional service across every mile.</p>
    </div>
  </div>
</section>
