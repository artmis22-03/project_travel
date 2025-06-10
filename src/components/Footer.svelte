<script>
  const year = new Date().getFullYear();
</script>

<footer class="bg-gray-900 text-gray-300 pt-10 pb-6">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-3 gap-8">

    <!-- About -->
    <div>
      <h2 class="text-xl font-bold text-white">SierraTravels</h2>
      <p class="mt-2 text-sm">
        Creating seamless travel experiences with custom packages, expert support, and unforgettable destinations.
      </p>
    </div>

    <!-- Quick Links -->
    <div>
      <h3 class="text-lg font-semibold text-white mb-2">Quick Links</h3>
      <ul class="space-y-1 text-sm">
        <li><a href="/" class="hover:underline">Home</a></li>
        <li><a href="/about" class="hover:underline">About</a></li>
        <li><a href="/packages" class="hover:underline">Services</a></li>
        <li><a href="/contact" class="hover:underline">Contact</a></li>
      </ul>
    </div>

    <!-- Contact -->
    <div>
      <h3 class="text-lg font-semibold text-white mb-2">Contact Us</h3>
      <p class="text-sm">Email: support@sierratravels.com</p>
      <p class="text-sm">Phone: +91 99999 99999</p>
      <p class="text-sm">Location: Bangalore, India</p>
    </div>
  </div>

  <!-- Divider -->
  <div class="mt-8 border-t border-gray-700 pt-4 flex flex-col md:flex-row justify-between items-center text-xs text-gray-500 px-4">
    <p>© {year} SierraTravels. All rights reserved.</p>

    <!-- Optional: Socials -->
    <div class="mt-2 md:mt-0 flex gap-4">
      <a href="#" aria-label="Instagram" class="hover:text-white">
        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
          <path d="M7.75 2A5.75 5.75 0 0 0 2 7.75v8.5A5.75 5.75 0 0 0 7.75 22h8.5A5.75 5.75 0 0 0 22 16.25v-8.5A5.75 5.75 0 0 0 16.25 2h-8.5Zm0 1.5h8.5A4.25 4.25 0 0 1 20.5 7.75v8.5a4.25 4.25 0 0 1-4.25 4.25h-8.5A4.25 4.25 0 0 1 3.5 16.25v-8.5A4.25 4.25 0 0 1 7.75 3.5Zm8.75 2a.75.75 0 1 0 0 1.5.75.75 0 0 0 0-1.5ZM12 7a5 5 0 1 0 0 10 5 5 0 0 0 0-10Zm0 1.5a3.5 3.5 0 1 1 0 7 3.5 3.5 0 0 1 0-7Z"/>
        </svg>
      </a>
      <a href="#" aria-label="Facebook" class="hover:text-white">
        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
          <path d="M13.5 2H10A6 6 0 0 0 4 8v4H1v4h3v8h4v-8h3l1-4h-4V8a2 2 0 0 1 2-2h3.5V2Z" />
        </svg>
      </a>
    </div>
  </div>
</footer>
