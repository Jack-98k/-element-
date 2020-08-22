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
  },
  methods: {
    eat () {
      console.log('马上回家')
    }
  }
}
</script>

<style scoped>
</style>
