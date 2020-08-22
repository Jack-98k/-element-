<template>
  <div>
    <h3>child1</h3>
  </div>
</template>

<script>
export default {
  name: 'child1',
  mounted () {
    this.$parent.$on('event-from-child2', function (msg) {
      console.log('Child1: ', msg)
    })
  }
}
</script>

<style scoped>
</style>
