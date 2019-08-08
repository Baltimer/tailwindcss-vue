<template>
  <nav class="px-4 py-2 w-full flex justify-between items-center">
    <div>
      <img class="h-8 w-auto" src="@/assets/img/logo.png" alt="logo">
    </div>
    <div>
      <button>
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 fill-current text-gray-500"><path d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"/></svg>
        <!-- <router-link to="/" class="mr-2 text-white">Home</router-link>
        <router-link to="/about" class="text-white">About</router-link> -->
      </button>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  props: {
    
  },
};
</script>

<style lang="scss" scoped>
.router-link-exact-active {
  color: blue;
}
</style>
