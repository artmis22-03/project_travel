<script lang="ts">
  import { onDestroy } from "svelte";

  interface Vehicle {
    name: string;
    image: string;
    passengers: string;
    type: string;
    capacity: string;
    rate: string;
    category: string;
    images?: string[];
    included?: string[];
    excluded?: string[];
  }

  const categories = ["Outstation", "Local", "Airport Drop"];
  let selectedCategory = "Outstation";

  const vehicles: Vehicle[] = [
  // Outstation
  {
    name: "Toyota Etios",
    image: "/images/etios1.png",
    images: ["/images/etios1.png", "/images/etios2.png", "/images/etios3.png"],
    passengers: "3 Passengers + 2 Bags",
    type: "SEDAN · DIESEL",
    capacity: "4+1",
    rate: "Rs.14 per KM",
    category: "Outstation",
    included: ["Fuel Charges"],
    excluded: [
      "Toll & Parking",
      "Driver Batta Rs.350/day (6AM–10PM)",
      "Driver Batta Rs.350/night (10PM–6AM)",
      "Night Stay Charges Rs.100/-"
    ]
  },
  {
    name: "Innova Crysta",
    image: "/images/innova1.png",
    images: ["/images/innova1.png", "/images/innova2.png", "/images/innova3.png"],
    passengers: "7 Passengers + 4 Bags",
    type: "MPV · DIESEL",
    capacity: "7+1",
    rate: "Rs.20 per KM",
    category: "Outstation",
    included: ["Fuel Charges"],
    excluded: [
      "Toll & Parking",
      "Driver Batta Rs.400/day (6AM–10PM)",
      "Driver Batta Rs.400/night (10PM–6AM)",
      "Night Stay Charges Rs.100/-"
    ]
  },
  {
    name: "Tempo Traveller BS6",
    image: "/images/traveller.png",
    images: ["/images/traveller1.png", "/images/traveller2.png"],
    passengers: "12 Passengers + 8 Bags",
    type: "DIESEL",
    capacity: "12+1",
    rate: "Rs.24 per KM",
    category: "Outstation",
    included: ["Fuel Charges"],
    excluded: [
      "Toll & Parking",
      "Driver Batta Rs.500/day (6AM–10PM)",
      "Driver Batta Rs.500/night (10PM–6AM)",
      "Night Stay Charges Rs.100/-"
    ]
  },

  // Local
  {
    name: "Swift Dzire",
    image: "/images/dzire.png",
    images: ["/images/dzire1.png", "/images/dzire2.png"],
    passengers: "3 Passengers + 2 Bags",
    type: "SEDAN · PETROL",
    capacity: "4+1",
    rate: "Rs.800 for 8hrs/80KM",
    category: "Local",
    included: ["Driver & Fuel"],
    excluded: ["Extra KM Rs.12", "Extra Hour Rs.100"]
  },
  {
    name: "Ertiga",
    image: "/images/ertiga.png",
    images: ["/images/ertiga1.png", "/images/ertiga2.png"],
    passengers: "6 Passengers + 3 Bags",
    type: "MPV · PETROL",
    capacity: "6+1",
    rate: "Rs.1200 for 8hrs/80KM",
    category: "Local",
    included: ["Driver & Fuel"],
    excluded: ["Extra KM Rs.15", "Extra Hour Rs.150"]
  },

  // Airport Drop
  {
    name: "Innova Crysta (Airport Drop)",
    image: "/images/innova-airport.png",
    images: ["/images/innova-airport.png"],
    passengers: "6 Passengers + 3 Bags",
    type: "MPV · DIESEL",
    capacity: "6+1",
    rate: "Rs.1500 per trip",
    category: "Airport Drop",
    included: ["Fuel & Driver"],
    excluded: ["Parking & Toll"]
  },
  {
    name: "Sedan (Airport Drop)",
    image: "/images/etios-airport.png",
    images: ["/images/etios-airport.png"],
    passengers: "3 Passengers + 2 Bags",
    type: "SEDAN · PETROL",
    capacity: "4+1",
    rate: "Rs.900 per trip",
    category: "Airport Drop",
    included: ["Fuel & Driver"],
    excluded: ["Parking & Toll"]
  }
];


  let selectedVehicle: Vehicle | null = null;
  let currentImageIndex = 0;
  let interval: ReturnType<typeof setInterval>;

  function handleKnowMore(vehicle: Vehicle) {
    selectedVehicle = vehicle;
    currentImageIndex = 0;
    setupAutoSlide();
  }

  function nextImage() {
    if (selectedVehicle?.images) {
      currentImageIndex = (currentImageIndex + 1) % selectedVehicle.images.length;
    }
  }

  function prevImage() {
    if (selectedVehicle?.images) {
      currentImageIndex = (currentImageIndex - 1 + selectedVehicle.images.length) % selectedVehicle.images.length;
    }
  }

  function setupAutoSlide() {
    clearInterval(interval);
    if (selectedVehicle?.images?.length && selectedVehicle.images.length > 1) {
      interval = setInterval(() => {
        nextImage();
      }, 3000);
    }
  }

  onDestroy(() => {
    clearInterval(interval);
  });

  $: filteredVehicles = vehicles.filter(v => v.category === selectedCategory);
</script>

<style>
  .fade {
    transition: opacity 0.5s ease-in-out;
  }
</style>
<!-- Spacing Section -->
<div class="my-16"></div>

<!-- Category Buttons -->
<div class="flex justify-center gap-4 mb-10">
  {#each categories as cat}
    <button
      on:click={() => { selectedCategory = cat; selectedVehicle = null; }}
      class="px-4 py-2 font-semibold rounded text-white transition duration-300"
      class:bg-blue-900={selectedCategory === cat}
      class:bg-red-600={selectedCategory !== cat}>
      {cat}
    </button>
  {/each}
</div>

<!-- Vehicle Cards -->
{#if !selectedVehicle}
  <!-- Cards Grid -->
  <div class="grid gap-6 sm:grid-cols-2 md:grid-cols-3 max-w-7xl mx-auto mb-12">
    {#each filteredVehicles as vehicle}
      <div class="bg-white rounded-2xl shadow hover:shadow-lg transition p-4">
        <img src={vehicle.image} alt={vehicle.name} class="w-full h-40 object-cover rounded-xl mb-4" />
        <h2 class="text-xl font-semibold text-gray-800">{vehicle.name}</h2>
        <p class="text-sm text-gray-600 mt-1">{vehicle.passengers}</p>
        <p class="text-sm text-gray-600">{vehicle.type}</p>
        <p class="text-sm text-gray-800 font-medium mt-2">Capacity: {vehicle.capacity}</p>
        <p class="text-sm text-gray-800 font-medium">Rate: {vehicle.rate}</p>
        <button
          on:click={() => handleKnowMore(vehicle)}
          class="mt-4 w-full bg-blue-600 text-white py-2 px-4 rounded-lg text-sm font-medium hover:bg-blue-700 transition duration-300 ease-in-out">
          Know More
        </button>
      </div>
    {/each}
  </div>
  <div class="w-full bg-white border-t-4 border-blue-500 mt-12">
      <div class="max-w-7xl mx-auto px-6 py-8">
        <h2 class="text-2xl font-bold text-blue-700 mb-4">Terms and Conditions</h2>
        <ul class="list-disc pl-6 space-y-2 text-gray-800 text-sm">
          <li>Toll, State Tax, Entry Fee & Parking at actuals.</li>
          <li>The KMS & Hours usage will be calculated from Office to Office (JP Nagar).</li>
          <li>
            Cancellation charges:
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
    <!-- Spacing Section -->


{:else}
  <!-- Detailed View -->
  <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-8 bg-white shadow-lg rounded-xl overflow-hidden p-6">
    <div class="relative">
      {#if selectedVehicle.images}
        <img
          src={selectedVehicle.images[currentImageIndex]}
          alt="Vehicle Image"
          class="object-cover max-h-[500px] w-full rounded fade"
          key={selectedVehicle.images[currentImageIndex]} />
      {/if}
      <button on:click={prevImage} class="absolute top-1/2 left-0 transform -translate-y-1/2 bg-white text-gray-700 p-2 rounded-r shadow hover:bg-gray-100">❮</button>
      <button on:click={nextImage} class="absolute top-1/2 right-0 transform -translate-y-1/2 bg-white text-gray-700 p-2 rounded-l shadow hover:bg-gray-100">❯</button>
    </div>

    <div>
      <h2 class="text-3xl font-bold text-gray-800 mb-4">{selectedVehicle.name}</h2>
      <p class="text-gray-600 text-sm mb-1">{selectedVehicle.passengers}</p>
      <p class="text-gray-600 text-sm mb-1">{selectedVehicle.type}</p>
      <p class="text-gray-800 font-semibold mb-1">Capacity: {selectedVehicle.capacity}</p>
      <p class="text-gray-800 font-semibold mb-4">Rate: {selectedVehicle.rate}</p>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-6 text-sm">
        <div>
          <h3 class="font-semibold text-green-700 mb-1">Included</h3>
          <ul class="list-disc list-inside space-y-1 text-gray-700">
            {#each selectedVehicle.included ?? [] as item}
              <li>{item}</li>
            {/each}
          </ul>
        </div>
        <div>
          <h3 class="font-semibold text-red-700 mb-1">Excluded</h3>
          <ul class="list-disc list-inside space-y-1 text-gray-700">
            {#each selectedVehicle.excluded ?? [] as item}
              <li>{item}</li>
            {/each}
          </ul>
        </div>
      </div>

      <button on:click={() => (selectedVehicle = null)} class="mt-6 bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700 transition duration-300">
        Back to List
      </button>
    </div>
  </div>
{/if}


