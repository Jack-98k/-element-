<template>
  <div id="app">
    <!-- <communicate></communicate> -->
    <LuoForm></LuoForm>
  </div>
</template>

<script>
// import communicate from '@/components/communication'
import LuoForm from '@/components/LuoForm'
export default {
  name: 'App',
  components: {
    // communicate
    LuoForm
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
