<template>
  <div>
    <welcome />
    <recent-sets />
    <videos />
    <releases />
  </div>
</template>

<script>
export default {
  components: {
    Releases: () => import('@/components/Releases'),
    RecentSets: () => import('@/components/RecentSets'),
    Videos: () => import('@/components/Videos'),
    Welcome: () => import('@/components/Welcome')
  }
}
</script>
