<template>
  <div>
    <bio />
    <!-- <recent-sets />
    <videos />
     <releases />-->
  </div>
</template>

<script>
export default {
  components: {
    // Releases: () => import('@/views/Releases'),
    // RecentSets: () => import('@/views/RecentSets'),
    // Videos: () => import('@/views/Videos'),
    Bio: () => import('@/views/Bio')
  }
}
</script>
