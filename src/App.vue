<template>
  <div id="app" class="h-full bg-gray-200">
    <header class="bg-gray-900">
      <NavBar></NavBar>
    </header>
    <section class="bg-gray-800 pl-4 pr-2 py-3 flex justify-between">
      <div class="relative">
        <div class="absolute inset-y-0 left-0 pl-3 flex items-center">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 fill-current text-gray-500" viewBox="0 0 24 24"><path d="M16.32 14.9l5.39 5.4a1 1 0 0 1-1.42 1.4l-5.38-5.38a8 8 0 1 1 1.41-1.41zM10 16a6 6 0 1 0 0-12 6 6 0 0 0 0 12z"/></svg>
        </div>
        <input class="block w-full border border-transparent bg-gray-900 focus:outline-none focus:bg-white focus:text-gray-900 text-white rounded-lg pl-10 pr-4 py-2" type="text" placeholder="Búsqueda">
      </div>
      <button class="flex items-center bg-gray-700 hover:bg-gray-600 focus:outline-none focus:shadow-outline rounded-lg shadow pr-4 pl-3 ml-4">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 fill-current text-gray-500" viewBox="0 0 24 24"><path d="M2.3 7.7A1 1 0 0 1 2 7V3a1 1 0 0 1 1-1h18a1 1 0 0 1 1 1v4a1 1 0 0 1-.3.7L15 14.42V17a1 1 0 0 1-.3.7l-4 4A1 1 0 0 1 9 21v-6.59l-6.7-6.7zM4 4v2.59l6.7 6.7a1 1 0 0 1 .3.71v4.59l2-2V14a1 1 0 0 1 .3-.7L20 6.58V4H4z"/></svg>
        <span class="ml-1 text-white text-medium">Filtros</span>
        </button>
    </section>
    <main>
      <router-view/>
    </main>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'

export default {
  components: {
    "NavBar": NavBar
  }
}
</script>