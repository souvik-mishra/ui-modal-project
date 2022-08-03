<template>
  <div v-if="showModal">
    <Modal
      :header="modalHeader"
      :text="modalBodyText"
      @closeModal="showModal = false"
    />
  </div>
  <h1>{{ message }}</h1>
  <input type="text" ref="name" />
  <button @click="handleClick">Click Me!</button>
  <br />
  <br />
  <button @click="toggleModal">Show Modal!</button>
</template>

<script>
// @ is an alias to /src
import Modal from "../components/Modal.vue";

export default {
  name: "Home",
  components: { Modal },
  data() {
    return {
      message: "Welcome to Vue 3",
      showModal: false,
      modalHeader: "Howdy Fellas",
      modalBodyText: "Let me know your queries",
    };
  },
  methods: {
    handleClick() {
      //Get the DOM object with this.$refs.name
      alert("Too much fun :P");
    },
    toggleModal() {
      this.showModal = !this.showModal;
    },
  },
};
</script>

<style>
h1 {
  border-bottom: 1px solid #d6d4d4;
}
</style>
