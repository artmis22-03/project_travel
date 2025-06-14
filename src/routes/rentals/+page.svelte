<script lang="ts">
  interface Vehicle {
    name: string;
    image: string;
    passengers: string;
    type: string;
    capacity: string;
    rate: string;
    images?: string[];
  }

  const vehicles: Vehicle[] = [
    {
      name: "Toyota Etios",
      image: "/images/etios.png",
      images: ["/images/etios1.png", "/images/etios2.png", "/images/etios3.png"],
      passengers: "3 Passengers + 2 Bags",
      type: "SEDAN · DIESEL",
      capacity: "4+1",
      rate: "Rs.14 per KM"
    },
    {
      name: "Innova Crysta",
      image: "/images/innova.png",
      images: ["/images/innova1.png", "/images/innova2.png", "/images/innova3.png"],
      passengers: "6 Passengers + 3 Bags",
      type: "SUV · DIESEL",
      capacity: "6+1",
      rate: "Rs.18 per KM"
    },
    {
      name: "Swift Dzire",
      image: "/images/swift.png",
      images: ["/images/swift1.png", "/images/swift2.png", "/images/swift3.png"],
      passengers: "3 Passengers + 2 Bags",
      type: "SEDAN · PETROL",
      capacity: "4+1",
      rate: "Rs.13 per KM"
    }
  ];

  let selectedVehicle: Vehicle | null = null;
  let currentImageIndex = 0;

  function handleKnowMore(vehicle: Vehicle) {
    selectedVehicle = vehicle;
    currentImageIndex = 0;
  }

  function nextImage() {
    if (selectedVehicle && selectedVehicle.images) {
      currentImageIndex = (currentImageIndex + 1) % selectedVehicle.images.length;
    }
  }

  function prevImage() {
    if (selectedVehicle && selectedVehicle.images) {
      currentImageIndex = (currentImageIndex - 1 + selectedVehicle.images.length) % selectedVehicle.images.length;
    }
  }
</script>

<div class="min-h-screen bg-gray-100 py-10 px-4">
  <h1 class="text-3xl font-bold text-center text-gray-800 mb-10">Rental Vehicles</h1>

  {#if !selectedVehicle}
    <!-- Vehicle Cards -->
    <div class="grid gap-6 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 max-w-7xl mx-auto mb-12">
      {#each vehicles as vehicle}
        <div class="bg-white rounded-2xl shadow hover:shadow-lg transition p-4">
          <img
            src={vehicle.image}
            alt={vehicle.name}
            class="w-full h-40 object-cover rounded-xl mb-4"
          />
          <h2 class="text-xl font-semibold text-gray-800">{vehicle.name}</h2>
          <p class="text-sm text-gray-600 mt-1">{vehicle.passengers}</p>
          <p class="text-sm text-gray-600">{vehicle.type}</p>
          <p class="text-sm text-gray-800 font-medium mt-2">Capacity: {vehicle.capacity}</p>
          <p class="text-sm text-gray-800 font-medium">Rate: {vehicle.rate}</p>
          <button
            class="mt-4 w-full bg-blue-600 hover:bg-blue-700 text-white py-2 px-4 rounded-lg text-sm font-medium"
            on:click={() => handleKnowMore(vehicle)}
          >
            Know More
          </button>
        </div>
      {/each}
    </div>

    <!-- Terms and Conditions - Full Width -->
    <div class="w-full bg-white border-t-4 border-blue-500 mt-12">
      <div class="max-w-7xl mx-auto px-6 py-8">
        <h2 class="text-2xl font-bold text-blue-700 mb-4">Terms and Conditions</h2>
        <ul class="list-disc pl-6 space-y-2 text-gray-800 text-sm">
          <li>Toll, State Tax, Entry Fee & Parking at actuals.</li>
          <li>The KMS & Hours usage will be calculated from Office to Office (JP Nagar).</li>
          <li>
            Cancellation charges will be applicable:
            <ul class="list-disc pl-6 mt-1">
              <li>75% if cancelled 72 hrs prior</li>
              <li>50% if cancelled 48 hrs prior</li>
              <li>100% if cancelled 24 hrs prior</li>
            </ul>
          </li>
          <li>GST of 5% is applicable.</li>
        </ul>
      </div>
    </div>

  {:else}
    <!-- Vehicle Detail View -->
    <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-8 bg-white shadow-lg rounded-xl overflow-hidden p-6">
      <!-- Left: Image Carousel -->
      <div class="relative">
        <img
          src={selectedVehicle.images[currentImageIndex]}
          alt="Vehicle Image"
          class="object-cover max-h-[500px] w-full rounded"
        />
        <button on:click={prevImage} class="absolute top-1/2 left-0 transform -translate-y-1/2 bg-white text-gray-700 p-2 rounded-r shadow">❮</button>
        <button on:click={nextImage} class="absolute top-1/2 right-0 transform -translate-y-1/2 bg-white text-gray-700 p-2 rounded-l shadow">❯</button>
      </div>

      <!-- Right: Details -->
      <div>
        <h2 class="text-3xl font-bold text-gray-800 mb-4">{selectedVehicle.name}</h2>
        <p class="text-gray-600 text-sm mb-2">{selectedVehicle.passengers}</p>
        <p class="text-gray-600 text-sm mb-2">{selectedVehicle.type}</p>
        <p class="text-gray-800 font-semibold mb-1">Capacity: {selectedVehicle.capacity}</p>
        <p class="text-gray-800 font-semibold mb-4">Rate: {selectedVehicle.rate}</p>

        <h3 class="text-xl font-semibold text-blue-700 mt-8 mb-2">Terms and Conditions</h3>
        <ul class="list-disc pl-5 text-gray-700 text-sm space-y-1">
          <li>Toll, State Tax, Entry Fee & Parking at actuals.</li>
          <li>The KMS & Hours usage will be calculated from Office to Office (JP Nagar).</li>
          <li>
            Cancellation charges apply:
            <ul class="list-disc pl-5">
              <li>75% if cancelled 72 hrs prior</li>
              <li>50% if cancelled 48 hrs prior</li>
              <li>100% if cancelled 24 hrs prior</li>
            </ul>
          </li>
          <li>GST of 5% is applicable.</li>
        </ul>

        <button on:click={() => (selectedVehicle = null)} class="mt-6 bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">
          Back to List
        </button>
      </div>
    </div>
  {/if}
</div>