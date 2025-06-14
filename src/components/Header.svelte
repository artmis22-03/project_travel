<script>
  let isOpen = false;
  let servicesOpen = false; // for mobile "Services" toggle
</script>

<header class="sticky top-0 z-5 bg-white shadow-md">
  <div class="min-h-16 bg-gray-100">
    <!-- Navbar -->
    <nav class="bg-white shadow">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16">
          <div class="flex">
            <div class="flex-shrink-0 flex items-center text-2xl font-bold text-blue-600">
              SierraTravels
            </div>

            <!-- Desktop Menu -->
            <div class="hidden md:flex md:items-center md:space-x-8 ml-10">
              <a href="/" class="text-gray-700 hover:text-blue-600 px-3 py-2 rounded-md">Home</a>
              <a href="/aboutus" class="text-gray-700 hover:text-blue-600 px-3 py-2 rounded-md">About</a>

              <!-- Services dropdown on hover (desktop) -->
              <div class="relative group">
                <div class="inline-flex items-center px-2 py-3 text-gray-700 hover:text-blue-600 cursor-pointer">
                  Services
                  <svg class="ml-1 w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                  </svg>
                </div>
                <div
                  class="absolute z-40 w-48 bg-white border border-gray-200 rounded shadow-lg opacity-0 group-hover:opacity-100 group-hover:visible invisible transition-opacity duration-200"
                >
                  <a href="/rentals" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Vehicle Rentals</a>
                  <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Employee Transportation</a>
                </div>
              </div>

              <a href="/contactus" class="text-gray-700 hover:text-blue-600 px-3 py-2 rounded-md">Contact Us</a>
            </div>
          </div>

          <!-- Mobile menu button -->
          <div class="md:hidden flex items-center">
            <button on:click={() => isOpen = !isOpen} class="text-gray-700 hover:text-blue-600 focus:outline-none">
              <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                {#if isOpen}
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                {:else}
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                {/if}
              </svg>
            </button>
          </div>
        </div>
      </div>

      <!-- Mobile Menu -->
      {#if isOpen}
        <div class="md:hidden bg-white border-t border-gray-200">
          <a href="/" class="block px-4 py-2 text-gray-700 hover:bg-gray-100" on:click={() => isOpen = false}>Home</a>
          <a href="/aboutus" class="block px-4 py-2 text-gray-700 hover:bg-gray-100" on:click={() => isOpen = false}>About</a>

          <!-- Services Toggle in Mobile -->
          <div class="block border-t border-gray-200">
            <button 
              on:click={() => servicesOpen = !servicesOpen} 
              class="w-full flex justify-between items-center px-4 py-2 text-gray-700 font-semibold hover:bg-gray-100"
            >
              Services
              <svg 
                class="h-4 w-4 transform transition-transform duration-200"
                style:transform={servicesOpen ? 'rotate(90deg)' : 'rotate(0deg)'}
                fill="none" stroke="currentColor" viewBox="0 0 24 24"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
              </svg>
            </button>

            {#if servicesOpen}
              <div class="pl-8 pr-4">
                <a href="/rentals" class="block py-2 text-gray-800 hover:bg-gray-100 rounded" on:click={() => isOpen = false}>Vehicle Rentals</a>
                <a href="#" class="block py-2 text-gray-800 hover:bg-gray-100 rounded" on:click={() => isOpen = false}>Employee Transportation</a>
              </div>
            {/if}
          </div>

          <a href="/contactus" class="block px-4 py-2 text-gray-700 hover:bg-gray-100" on:click={() => isOpen = false}>Contact Us</a>
        </div>
      {/if}
    </nav>
  </div>
</header>

<!-- WhatsApp Floating Button -->
<a 
  href="https://wa.me/919999999999" 
  target="_blank" 
  class="fixed bottom-4 right-4 bg-[#25D366] text-white p-3 rounded-full shadow-lg flex items-center justify-center hover:bg-green-500 transition duration-300 z-50"
  aria-label="Chat on WhatsApp"
>
  <img src="/whatsapp-symbol-logo-svgrepo-com.svg" alt="WhatsApp" class="h-5 w-5 md:mr-2" />
  <span class="hidden md:inline text-sm font-semibold">Chat on WhatsApp</span>
</a>