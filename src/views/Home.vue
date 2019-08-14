<template>
  <main class="py-6 xl:flex-1 xl:overflow-x-hidden">
    <div class="px-4">
      <h3 class="text-gray-900 text-xl">Casas</h3>
      <p class="text-gray-600">Encuentra las casas que necesites!</p>
    </div>
    <div class="mt-6 sm:overflow-x-auto">
      <div class="px-4 sm:inline-flex sm:-ml-2 sm:pb-8">
        <div v-for="(property, i) in properties" :key="i" :class="{ 'mt-10': i > 0 }" class="sm:mt-0 sm:max-w-xs sm:w-80 sm:flex-shrink-0 sm:px-2">
          <PropertyCard :property="property" />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import PropertyCard from '@/components/PropertyCard'

export default {
  name: 'home',
  components: {
    PropertyCard
  },
  data(){
    return {
      properties: [
        {
          imgUrl: "./assets/img/home1.jpg",
          beds: 3,
          baths: 2,
          title: "Casa moderna en el centro",
          price: 140000,
          reviewCount: 34,
          rating: 4
        },
        {
          imgUrl: "./assets/img/home1.jpg",
          beds: 3,
          baths: 2,
          title: "Casa moderna en el centro",
          price: 140000,
          reviewCount: 34,
          rating: 4
        },
        {
          imgUrl: "../img/home1.jpg",
          beds: 3,
          baths: 2,
          title: "Casa moderna en el centro",
          price: 140000,
          reviewCount: 34,
          rating: 4
        },
        {
          imgUrl: "./assets/img/home1.jpg",
          beds: 3,
          baths: 2,
          title: "Casa moderna en el centro",
          price: 140000,
          reviewCount: 34,
          rating: 4
        }
      ]
    }
  }
};
</script>
