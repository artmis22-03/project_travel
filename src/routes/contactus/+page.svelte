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
    <h1
      class="text-5xl font-extrabold text-center text-blue-800 mb-12 tracking-tight"
      data-aos="fade-down"
    >
      Contact Us
    </h1>

    <div class="grid md:grid-cols-2 gap-8 mb-16">
      <!-- Contact Info -->
      <div
        class="bg-gradient-to-br from-pink-150 to-pink-200 p-8 rounded-3xl shadow-xl"
        data-aos="fade-right"
      >
        <h2 class="text-2xl font-semibold text-blue-700 mb-6">Contact Information</h2>
        <div class="space-y-4 font-medium text-lg">
          <p><strong>📞 Phone:</strong> +91 99723 10009</p>
          <p><strong>✉️ Email:</strong> mails@sierratravels.com</p>
          <p><strong>📍 Address:</strong> No.135, 2nd Floor, East End 4th Main, JP Nagar 3rd Phase, Bangalore, 560078</p>
        </div>

        <!-- WhatsApp Button -->
        <div class="mt-6" data-aos="fade-up" data-aos-delay="200">
          <a
            href="https://wa.me/919972310009"
            target="_blank"
            class="inline-flex items-center gap-2 bg-green-500 hover:bg-green-600 text-white font-medium px-5 py-2 rounded-xl shadow-md transition"
          >
            <img src="/whatsapp-symbol-logo-svgrepo-com.svg" alt="WhatsApp" class="w-5 h-5" />
            Chat on WhatsApp
          </a>
        </div>

        <!-- Map -->
        <div class="text-center max-w-md mx-auto font-medium text-lg mt-6" data-aos="zoom-in" data-aos-delay="400">
          <iframe
            title="Sierra Travels Location Map"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3888.867745649355!2d77.597606!3d12.916220700000002!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bae15f897c7d377%3A0x6028602efc8a7779!2sSIERRA%20TRAVELS!5e0!3m2!1sen!2sin!4v1751292727504!5m2!1sen!2sin"
            width="100%"
            height="250"
            class="rounded-xl shadow-lg"
            style="border:0;"
            allowfullscreen
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
      </div>

      <!-- Enquiry Form -->
      <div
        class="bg-white p-8 rounded-3xl shadow-xl"
        data-aos="fade-left"
      >
        <h2 class="text-2xl font-semibold text-blue-700 mb-6">Enquiry Form</h2>
        <form
          action="mailto:mails@sierratravels.com"
          method="POST"
          enctype="text/plain"
          class="space-y-5"
        >
          <div data-aos="fade-up" data-aos-delay="200">
            <label for="name" class="block text-sm font-medium text-gray-600">Name</label>
            <input
              id="name"
              type="text"
              name="Name"
              class="w-full mt-1 border border-gray-300 rounded-xl px-4 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
              required
            />
          </div>
          <div data-aos="fade-up" data-aos-delay="300">
            <label for="email" class="block text-sm font-medium text-gray-600">Email</label>
            <input
              id="email"
              type="email"
              name="Email"
              class="w-full mt-1 border border-gray-300 rounded-xl px-4 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
              required
            />
          </div>
          <div data-aos="fade-up" data-aos-delay="400">
            <label for="message" class="block text-sm font-medium text-gray-600">Message</label>
            <textarea
              id="message"
              name="Message"
              rows="4"
              class="w-full mt-1 border border-gray-300 rounded-xl px-4 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
              required
            ></textarea>
          </div>
          <button
            type="submit"
            class="bg-blue-600 text-white px-6 py-2 rounded-xl hover:bg-blue-700 shadow-lg transition duration-200"
            data-aos="zoom-in"
            data-aos-delay="600"
          >
            Submit
          </button>
        </form>
      </div>
    </div>

    <!-- Additional About Text -->
    <div
      class="text-center max-w-3xl mx-auto font-medium text-lg"
      data-aos="fade-up"
      data-aos-delay="300"
    >
      <p>
        At <span class="font-semibold text-blue-700">SierraTravels</span>, we aim to make your journey smooth, comfortable, and memorable.
        Whether it's a weekend getaway or a business trip, our fleet of well-maintained vehicles and professional service ensures your travel needs are met with excellence.
        Customer satisfaction is our priority, and we look forward to being part of your travel story.
      </p>
    </div>
  </div>
</div>
