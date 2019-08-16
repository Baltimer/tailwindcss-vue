<template>
  <section class="bg-gray-800 xl:w-72">
    <div class="pl-4 pr-2 py-3 flex justify-between xl:hidden">
      <div class="relative max-w-xs w-full">
        <div class="absolute inset-y-0 left-0 pl-3 flex items-center">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 fill-current text-gray-600" viewBox="0 0 24 24"><path d="M16.32 14.9l5.39 5.4a1 1 0 0 1-1.42 1.4l-5.38-5.38a8 8 0 1 1 1.41-1.41zM10 16a6 6 0 1 0 0-12 6 6 0 0 0 0 12z"/></svg>
        </div>
        <input class="block w-full border border-transparent bg-gray-900 focus:outline-none focus:bg-white focus:text-gray-900 text-white rounded-lg pl-10 pr-4 py-2" type="text" placeholder="Búsqueda">
      </div>
      <button type="button" class="flex items-center focus:outline-none  rounded-lg pr-4 pl-3 ml-4"
        @click="toggle"
        :class="{ 'bg-gray-600 hover:bg-gray-700': isOpen, 'bg-gray-700 hover:bg-gray-600': !isOpen }"
      >
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 fill-current text-gray-500" viewBox="0 0 24 24"><path d="M2.3 7.7A1 1 0 0 1 2 7V3a1 1 0 0 1 1-1h18a1 1 0 0 1 1 1v4a1 1 0 0 1-.3.7L15 14.42V17a1 1 0 0 1-.3.7l-4 4A1 1 0 0 1 9 21v-6.59l-6.7-6.7zM4 4v2.59l6.7 6.7a1 1 0 0 1 .3.71v4.59l2-2V14a1 1 0 0 1 .3-.7L20 6.58V4H4z"/></svg>
        <span class="ml-1 text-white text-medium">Filtros</span>
      </button>
    </div>
    <form class=" xl:h-full xl:flex xl:flex-col xl:justify-between xl:h-full" :class="{ 'hidden': !isOpen, 'block': isOpen }">
      <div class="lg:flex xl:block xl:overflow-y-auto">
        <div class="px-4 py-4 border-t border-gray-900 lg:w-1/3 xl:border-t-0 xl:w-full">
          <div class="flex flex-wrap -mx-2">
            <label class="block w-1/2 sm:w-1/4 lg:w-1/2 px-2">
              <span class="text-sm font-semibold text-gray-500">Habitaciones</span>
              <select class="form-select block w-full mt-1 shadow">
                <option value="4">4</option>
              </select>
            </label>
            <label class="block w-1/2 sm:w-1/4 lg:w-1/2 px-2">
              <span class="text-sm font-semibold text-gray-500">Baños</span>
              <select class="form-select block w-full mt-1 shadow">
                <option value="2">2</option>
              </select>
            </label>
            <label class="block w-full px-2 mt-4 sm:mt-0 sm:w-1/2 lg:w-full">
              <span class="text-sm font-semibold text-gray-500">Rango de precios</span>
              <select class="mt-1 w-full form-select block shadow">
                <option value="">Hasta 200€/día</option>
              </select>
            </label>
          </div>
        </div>
        <div class="px-4 py-2 border-t border-gray-900 lg:w-1/3 lg:border-l xl:w-full">
          <span class="block text-sm font-semibold text-gray-500">Tipo de propiedad</span>
          <div class="sm:flex sm:-mx-2 lg:block lg:mx-0">
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-full lg:px-0">
              <input class="form-radio bg-gray-900 border-transparent" type="radio" name="type" value="house">
              <span class="ml-2 text-white">Casa</span>
            </label>
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-full lg:px-0">
              <input class="form-radio bg-gray-900 border-transparent" type="radio" name="type" value="apartment">
              <span class="ml-2 text-white">Apartamento</span>
            </label>
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-full lg:px-0">
              <input class="form-radio bg-gray-900 border-transparent" type="radio" name="type" value="Loft">
              <span class="ml-2 text-white">Loft</span>
            </label>
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-full lg:px-0">
              <input class="form-radio bg-gray-900 border-transparent" type="radio" name="type" value="townhouse">
              <span class="ml-2 text-white">Casa de pueblo</span>
            </label>
          </div>
        </div>
        <div class="px-4 py-2 border-t border-gray-900 lg:w-1/3 lg:border-l xl:w-full">
          <span class="block text-sm font-semibold text-gray-500">Características</span>
          <div class="sm:flex sm:-mx-2 sm:flex-wrap">
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-1/2 xl:w-full">
              <input class="form-checkbox bg-gray-900 border-transparent" type="checkbox" name="balcon">
              <span class="ml-2 text-white">Balcón</span>
            </label>
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-1/2 xl:w-full">
              <input class="form-checkbox bg-gray-900 border-transparent" type="checkbox" name="piscina">
              <span class="ml-2 text-white">Piscina</span>
            </label>
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-1/2 xl:w-full">
              <input class="form-checkbox bg-gray-900 border-transparent" type="checkbox" name="playa">
              <span class="ml-2 text-white">Playa</span>
            </label>
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-1/2 xl:w-full">
              <input class="form-checkbox bg-gray-900 border-transparent" type="checkbox" name="pet_friendly">
              <span class="ml-2 text-white">Pet friendly</span>
            </label>
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-1/2 xl:w-full">
              <input class="form-checkbox bg-gray-900 border-transparent" type="checkbox" name="kid_friendly">
              <span class="ml-2 text-white">Kid friendly</span>
            </label>
            <label class="flex sm:w-1/4 sm:px-2 items-center mt-3 lg:w-1/2 xl:w-full">
              <input class="form-checkbox bg-gray-900 border-transparent" type="checkbox" name="parking">
              <span class="ml-2 text-white">Parking</span>
            </label>
            <label class="flex sm:w-1/2 sm:px-2 items-center mt-3 lg:w-full">
              <input class="form-checkbox bg-gray-900 border-transparent" type="checkbox" name="air_conditioned">
              <span class="ml-2 text-white">Aire acondicionado</span>
            </label>
          </div>
        </div>
      </div>
      <div class="bg-gray-900 px-4 py-2">
        <button class="block w-full xl:w-full sm:w-auto sm:inline-block bg-indigo-500 hover:bg-indigo-400 font-semibold text-white px-4 py-2 rounded-lg">Actualizar resultados</button>
      </div>
    </form>
  </section>
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
}
</script>
