<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <MyModal theme="" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>Ninja Giveaway</h1>
      <p>Grab your ninja swag for half price</p>
    </MyModal>
  </div>
  <button @click="toggleModal">close modal</button>
</template>

<script>
import MyModal from './components/MyModal.vue'

export default {
  name: 'App',
  components: { MyModal },
  data() {
    return {
      title: 'My First Vue App :)',
      header: 'Sign up for the Giveaway',
      text: 'Grab your ninja swag for half price',
      showModal: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    }
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
