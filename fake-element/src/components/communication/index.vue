<template>
  <div>
    <child1></child1>
    <child2></child2>
  </div>
</template>

<script>
import child1 from '@/components/communication/child1.vue'
import child2 from '@/components/communication/child2.vue'

export default {
  name: 'parent',
  components: {
    child1,
    child2
  }
}
</script>

<style scoped>
</style>
