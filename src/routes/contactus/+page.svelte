<script lang="ts">
  let name = "";
  let email = "";
  let message = "";

  function handleSubmit() {
    alert(`Thank you, ${name}. We have received your message.`);
    name = "";
    email = "";
    message = "";
  }
</script>

<div class="min-h-screen bg-gradient-to-br from-blue-50 to-white py-16 px-6">
  <div class="max-w-6xl mx-auto">
    <h1 class="text-5xl font-extrabold text-center text-blue-800 mb-12 tracking-tight">Contact Us</h1>

    <div class="grid md:grid-cols-2 gap-8 mb-16">
      <!-- Contact Info -->
      <div class="bg-white p-8 rounded-3xl shadow-xl">
  <h2 class="text-2xl font-semibold text-blue-700 mb-6">Contact Information</h2>
  <div class="space-y-4 text-gray-700 text-lg">
    <p><strong>📞 Phone:</strong> +91 98765 43210</p>
    <p><strong>✉️ Email:</strong> contact@vehiclerental.com</p>
    <p><strong>📍 Address:</strong> 123, JP Nagar, Bengaluru, Karnataka, India</p>
  </div>

  <!-- WhatsApp Button -->
  <div class="mt-6">
  <a
    href="https://wa.me/919876543210"
    target="_blank"
    class="inline-flex items-center gap-2 bg-green-500 hover:bg-green-600 text-white font-medium px-5 py-2 rounded-xl shadow-md transition"
  >
    <img src="/whatsapp-symbol-logo-svgrepo-com.svg" alt="WhatsApp" class="w-5 h-5" />
    Chat on WhatsApp
  </a>
</div>

</div>


      <!-- Enquiry Form -->
      <div class="bg-white p-8 rounded-3xl shadow-xl">
        <h2 class="text-2xl font-semibold text-blue-700 mb-6">Enquiry Form</h2>
        <form on:submit|preventDefault={handleSubmit} class="space-y-5">
          <div>
            <label class="block text-sm font-medium text-gray-600">Name</label>
            <input type="text" bind:value={name} class="w-full mt-1 border border-gray-300 rounded-xl px-4 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none" required />
          </div>
          <div>
            <label class="block text-sm font-medium text-gray-600">Email</label>
            <input type="email" bind:value={email} class="w-full mt-1 border border-gray-300 rounded-xl px-4 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none" required />
          </div>
          <div>
            <label class="block text-sm font-medium text-gray-600">Message</label>
            <textarea bind:value={message} rows="4" class="w-full mt-1 border border-gray-300 rounded-xl px-4 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none" required></textarea>
          </div>
          <button type="submit" class="bg-blue-600 text-white px-6 py-2 rounded-xl hover:bg-blue-700 shadow-lg transition duration-200">
            Submit
          </button>
        </form>
      </div>
    </div>

    <!-- Additional About Text -->
    <div class="text-center max-w-3xl mx-auto text-gray-700 text-lg">
      <p>
        At <span class="font-semibold text-blue-700">SierraTravels</span>, we aim to make your journey smooth, comfortable, and memorable.
        Whether it's a weekend getaway or a business trip, our fleet of well-maintained vehicles and professional service ensures your travel needs are met with excellence.
        Customer satisfaction is our priority, and we look forward to being part of your travel story.
      </p>
    </div>
  </div>
</div>
