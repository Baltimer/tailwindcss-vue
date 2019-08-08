<template>
  <div id="app" class="h-full bg-gray-200">
    <SiteHeader />
    <SearchFilters />
    <main>
      <router-view/>
    </main>
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