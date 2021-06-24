<template>
  <div id="app">
    <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full" @click="showModal">
      Open Modal!
    </button>
   
    <Modal v-show="isModalVisible" @close="closeModal"></Modal>
  </div>
</template>

<script>

import Modal from "./components/Modal";

export default {
  name: 'App',
  components: {
    Modal
  },
   data() {
    return {
      isModalVisible: false,
    };
  },
  methods: {
    showModal() {
      // Do something here to determine
      // if you should show modal
      this.isModalVisible = true;
    },
    closeModal() {
      // this will catch the close event
      // after you're done processing the login in the component
      this.isModalVisible = false;
    },
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
