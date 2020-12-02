<template>
  <button v-on:click="toggleClick">Show Modal</button>
  <div v-if="showModal">
    <!-- closeonclick="toggleClick" -->
    <Modal title="Modal " v-on:close="toggleClick" />
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  data() {
    return {
      showModal: false,
    };
  },
  methods: {
    toggleClick() {
      return (this.showModal = !this.showModal);
    },
  },
  components: {
    Modal,
  },
};
</script>

<style scoped>
button {
  border-radius: 28px;
  border: 1px solid #18ab29;
  display: inline-block;
  cursor: pointer;
  color: #f0eae200;
  font-family: Arial;
  font-size: 17px;
  padding: 16px 31px;
  text-decoration: none;
  text-shadow: 0px 1px 0px #2f6627;
  outline: none;
}

button:hover {
  background-color: #5cbf2a;
}
</style>
