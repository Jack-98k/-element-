<template>
  <div>
    <LuoFormItem lable="用户名">
      <LuoInput v-model="userInfo.username"></LuoInput>
    </LuoFormItem>
  </div>
</template>

<script>
import LuoInput from '@/components/LuoForm/LuoInput.vue'
import LuoFormItem from '@/components/LuoForm/LuoFormItem.vue'

export default {
  name: 'LuoForm',
  components: {
    LuoInput,
    LuoFormItem
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
