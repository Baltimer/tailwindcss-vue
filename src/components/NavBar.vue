<template>
  <nav class="h-12 bg-blue-700 px-4 py-2 w-full flex justify-between">
    <div class="py-2">
      <div class="h-4 w-4 bg-red-300 rounded-lg"></div>
    </div>
    <div>
      <router-link to="/" class="mr-2">Home</router-link>
      <router-link to="/about">About</router-link>
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