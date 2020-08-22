<template>
  <div>
    <!-- $listeners 会被展开并监听 -->
    <h3 v-on="$listeners">child2</h3>
    <button @click="comToChild1('xxxxx111x')">给child1发送消息</button>
    <p>{{ $attrs.msg }}</p>
  </div>
</template>

<script>
export default {
  name: 'child2',
  methods: {
    comToChild1 (message) {
      // 利用 $parent 派发事件
      this.$parent.$emit('event-from-child2', message)
    }
  }
}
</script>

<style scoped>
</style>
