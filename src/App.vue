<template>
  <div id="app" class="min-h-screen bg-gray-200 antialiased xl:flex xl:flex-col xl:h-screen">
    <SiteHeader class="xl:flex-shrink-0" />
    <div class="xl:flex-1 xl:flex xl:overflow-y-hidden">
      <SearchFilters />
      <router-view/>
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
