<template>
  <div id="app">
      <router-view />
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return{
      user: null,
    }
  },
  created() {
    // localStorage.setItem("url", 'http://127.0.0.1:8989/')
    localStorage.setItem("url", 'http://120.79.141.87:8989/')
  }
}
</script>

<style>
</style>
