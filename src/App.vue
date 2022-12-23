<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <Modal :header="header" :text="text" :theme="theme" @close="closeModal" />
  </div>
  <button @click="toggleModal">Show Modal</button>
</template>

<script>
import Modal from './components/Modal.vue';

export default {
  name: 'App',

  components: {
    Modal,
  },

  data() {
    return {
      header: 'Sign up for the Giveaway!',
      text: 'Get a free course today!',
      theme: 'sale',
      showModal: false,
    };
  },

  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },

    closeModal() {
      this.showModal = false;
    },
  },
};
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

h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
