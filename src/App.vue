<template>
  <h1>{{ title }}</h1>
  <div v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">Grap now</a>

        <a href="#">Register</a>
      </template>
      <h1>Khamurad Giveaway</h1>
      <p>Grab your Khamurad swags at half price</p>
    </Modal>
  </div>
  
  <!-- second modal -->
  <div v-if="showModalTwo">
    <Modal @close="toggleModalTwo">
      <h1>This is the second modal</h1>
      <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
    </Modal>
  </div>
  <br />
  <button @click="toggleModal">Open Modal</button>
  <button @click="toggleModalTwo">Open Second Modal</button>
</template>

<script>
import Modal from "./components/Model.vue";

export default {
  name: "App",
  components: {
    Modal,
  },
  data() {
    return {
      title: "My first vue app",
      header: "Sign up for the Giveaway!",
      text: "Grab your Khamurad fashion swags at half price",
      showModal: false,
      showModalTwo: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo;
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
