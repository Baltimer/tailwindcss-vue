<template>
  <div id="app" class="w-full h-full bg-gray-300">
    <NavBar></NavBar>
    <router-view/>
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