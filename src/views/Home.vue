<template>
  <main class="py-6 xl:flex-1 xl:overflow-x-hidden">
    <div class="px-4">
      <h3 class="text-gray-900 text-xl">Casas</h3>
      <p class="text-gray-600">Encuentra las casas que necesites.</p>
    </div>
    <div class="mt-6 sm:overflow-x-auto">
      <div class="px-4 sm:inline-flex sm:-ml-2 sm:pb-8">
        <div v-for="(property, i) in properties" :key="i" :class="{ 'mt-10': i > 0 }" class="sm:mt-0 sm:max-w-xs sm:w-80 sm:flex-shrink-0 sm:px-2">
          <PropertyCard :property="property" />
        </div>
      </div>
    </div>
    <div class="px-4">
      <h3 class="text-gray-900 text-xl">Villas</h3>
      <p class="text-gray-600">Las mejores villas a tu disposición.</p>
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
          imgUrl: "https://images.unsplash.com/photo-1543489822-c49534f3271f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1489&q=80",
          beds: 3,
          baths: 2,
          title: "Casa moderna en el centro",
          price: 300,
          reviewCount: 34,
          rating: 4
        },
        {
          imgUrl: "https://images.unsplash.com/photo-1553524789-59ac0ed1d2d2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80",
          beds: 3,
          baths: 1,
          title: "Casa moderna en el centro",
          price: 200,
          reviewCount: 19,
          rating: 3
        },
        {
          imgUrl: "https://images.unsplash.com/photo-1543489822-c49534f3271f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1489&q=80",
          beds: 1,
          baths: 1,
          title: "Casa moderna en el centro",
          price: 280,
          reviewCount: 24,
          rating: 5
        },
        {
          imgUrl: "https://images.unsplash.com/photo-1553524805-28dbfc2f84fd?ixlib=rb-1.2.1&auto=format&fit=crop&w=1491&q=80",
          beds: 3,
          baths: 2,
          title: "Casa moderna en el centro",
          price: 220,
          reviewCount: 37,
          rating: 4
        }
      ]
    }
  }
};
</script>
