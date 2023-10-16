<template>
  <h1>{{ title }}</h1>
  <MyModal />
</template>

<script>
import MyModal from './components/MyModal.vue'

export default {
  name: 'App',
  components: { MyModal },
  data() {
    return {
      title: 'My First Vue App :)'
    }
  },
  methods: {
    
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
