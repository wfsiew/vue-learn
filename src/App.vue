<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <teleport to=".modals" v-if="showModal">
    <MyModal theme="" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>Ninja Giveaway</h1>
      <p>Grab your ninja swag for half price</p>
    </MyModal>
  </teleport>
  <teleport to=".modals" v-if="showModalX">
    <MyModal @close="toggleModalX">
      <h1>Sign up to the newsletter</h1>
      <p>For updates and promo codes</p>
    </MyModal>
  </teleport>
  <button @click="toggleModal">close modal</button>
  <button @click="toggleModalX">close modalx</button>
</template>

<script>
import MyModal from './components/MyModal.vue'

export default {
  name: 'App',
  components: { MyModal },
  data() {
    return {
      title: 'My First Vue App :)',
      showModal: false,
      showModalX: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    },
    toggleModalX() {
      this.showModalX = !this.showModalX
    }
  },
}
</script>

<style>
#app, .modals {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
