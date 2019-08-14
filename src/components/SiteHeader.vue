<template>
  <header class="bg-gray-900 sm:flex sm:items-center sm:justify-between xl:bg-white">
    <div class="px-4 py-3 flex justify-between items-center xl:w-72 xl:bg-gray-900 xl:justify-center xl:py-5">
      <div>
        <img class="h-8 w-auto" src="@/assets/img/logo.png" alt="logo">
      </div>
      <div class="flex sm:hidden">
        <button @click="toggle" type="button" class="px-2 text-gray-500 hover:text-white focus:outline-none focus:text-white">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 fill-current">
            <path v-if="isOpen" d="M16.24 14.83a1 1 0 0 1-1.41 1.41L12 13.41l-2.83 2.83a1 1 0 0 1-1.41-1.41L10.59 12 7.76 9.17a1 1 0 0 1 1.41-1.41L12 10.59l2.83-2.83a1 1 0 0 1 1.41 1.41L13.41 12l2.83 2.83z"/>
            <path v-if="!isOpen" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"/>
          </svg>
          <!-- <router-link to="/" class="mr-2 text-white">Home</router-link>
          <router-link to="/about" class="text-white">About</router-link> -->
        </button>
      </div>
    </div>
    <nav class="sm:flex sm:items-center sm:px-4 xl:w-full xl:flex-1 xl:justify-between" :class="{ 'hidden': !isOpen, 'block': isOpen }">
      <div class="hidden xl:block xl:relative xl:max-w-xs xl:w-full">
        <div class="absolute inset-y-0 left-0 pl-3 flex items-center">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 fill-current text-gray-600" viewBox="0 0 24 24"><path d="M16.32 14.9l5.39 5.4a1 1 0 0 1-1.42 1.4l-5.38-5.38a8 8 0 1 1 1.41-1.41zM10 16a6 6 0 1 0 0-12 6 6 0 0 0 0 12z"/></svg>
        </div>
        <input class="block w-full border border-transparent bg-gray-300 focus:outline-none focus:bg-white focus:border-gray-300 text-gray-900 rounded-lg pl-10 pr-4 py-2" type="text" placeholder="Búsqueda">
      </div>
      <div class="sm:flex sm:items-center">
        <div class="px-2 pt-2 pb-5 border-b border-gray-800 sm:flex sm:border-b-0 sm:py-0 sm:px-0">
          <a href="#" class="block px-3 py-1 rounded leading-tight font-semibold text-white hover:bg-gray-800 sm:text-sm sm:px-2 xl:text-gray-900">Registra tu propiedad</a>
          <a href="#" class="mt-1 block px-3 py-1 rounded leading-tight font-semibold text-white hover:bg-gray-800 sm:mt-0 sm:text-sm sm:px-2 xl:text-gray-900 sm:ml-2">Viajes</a>
          <a href="#" class="mt-1 block px-3 py-1 rounded leading-tight font-semibold text-white hover:bg-gray-800 sm:mt-0 sm:text-sm sm:px-2 xl:text-gray-900 sm:ml-2">Mensajes</a>
        </div>
        <div class="px-5 py-5 sm:py-0 sm:ml-4 sm:px-0">
          <div class="flex items-center">
            <img class="h-10 w-10 sm:h-8 sm:w-8 object-cover rounded-full border-2 border-gray-600 xl:border-gray-300" src="@/assets/img/perfil.jpg" alt="">
            <span class="ml-4 text-gray-200 font-semibold sm:hidden">Silvia Hasenberger</span>
          </div>
          <div class="mt-5 sm:hidden">
            <a href="#" class="block text-gray-400 hover:text-white">Configuración</a>
            <a href="#" class="mt-3 block text-gray-400 hover:text-white">Soporte</a>
            <a href="#" class="mt-3 block text-gray-400 hover:text-white">Desconectar</a>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  props: [],
  data() {
    return {
      isOpen: false
    }
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>

<style lang="scss" scoped>
.router-link-exact-active {
  color: blue;
}
</style>
