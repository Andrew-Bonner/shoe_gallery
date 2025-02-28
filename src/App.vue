<template>
  <div class="p-10 bg-gray-100 min-h-screen">
    <h1 class="text-3xl font-bold text-center mb-8">Shoe Gallery</h1>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 justify-center">
      <div
        v-for="shoe in shoes"
        :key="shoe.id"
        class="bg-white p-4 rounded-lg shadow-lg flex flex-col items-center w-44 mx-auto">
        <h2 class="text-lg font-semibold mb-2 text-center">{{ shoe.name }}</h2>
        <p class="text-gray-600 mt-3 text-center text-sm">{{ shoe.description }}</p>
        <img
          :src="shoe.image"
          :alt="shoe.name"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      shoes: [
        { id: 1, name: "Nike Air Jordan", description: "A classic sneaker with timeless style.", image: "/images/air-jordan-1.webp" },
        { id: 2, name: "Adidas Yeezy", description: "A fashionable and comfortable sneaker.", image: "/images/yeezy-350.jpg" },
        { id: 3, name: "Puma RS-X", description: "A stylish shoe with retro vibes.", image: "/images/puma-rsx.jpg" },
        { id: 4, name: "New Balance 990", description: "A premium sneaker known for its comfort.", image: "/images/nb-990.webp" },
        { id: 5, name: "Converse Chuck Taylor", description: "A legendary sneaker for all occasions.", image: "/images/chuck-taylor.jpg" }
      ]
    };
  }
};
</script>

<style scoped>
</style>
