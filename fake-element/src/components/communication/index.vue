<template>
  <div>
    <child1></child1>
    <child2 msg='efewfewef' @click="onClick"></child2>
    <button @click="goHome">回家吃饭</button>
  </div>
</template>

<script>
import child1 from '@/components/communication/child1.vue'
import child2 from '@/components/communication/child2.vue'

export default {
  name: 'parent',
  provide () {
    return {
      foo: 'foewfjoewjowe'
    }
  },
  components: {
    child1,
    child2
  },
  methods: {
    goHome () {
      this.$children[0].eat()
    },
    onClick () {
      console.log('老爹的问候', this)
    }
  }
}
</script>

<style scoped>
</style>
