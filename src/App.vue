<template>
  <div id="app" class="h-full bg-gray-200">
    <SiteHeader />
    <div>
      <SearchFilters />
      <main class="bg-gray-200">
        <router-view/>
      </main>
    </div>
  </div>
</template>

<script>
import SiteHeader from '@/components/SiteHeader'
import SearchFilters from '@/components/SearchFilters'

export default {
  components: {
    SiteHeader,
    SearchFilters
  }
}
</script>

<style lang="scss">
* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
}
</style>
