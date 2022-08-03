<template>
  <h1>{{ message }}</h1>
  <input type="text" ref="name" />
  <button @click="handleClick">Click Me!</button>
  <Modal />
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
    };
  },
  methods: {
    handleClick() {
      //Get the DOM object with this.$refs.name
      alert("Too much fun :P");
    },
  },
};
</script>

<style>
h1 {
  border-bottom: 1px solid #d6d4d4;
}
</style>
