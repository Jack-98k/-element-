<template>
  <div>
    <LuoInput></LuoInput>
  </div>
</template>

<script>
import LuoInput from '@/components/LuoForm/LuoInput.vue'
export default {
  name: 'LuoForm',
  components: {
    LuoInput
  },
  data () {
    return {
      userInfo: {
        username: '',
        password: ''
      },
      rules: {
        username: [{ required: true, message: '请输入用户名称' }],
        password: [{ required: true, message: '请输入密码' }]
      }
    }
  }
}
</script>

<style scoped>
</style>
