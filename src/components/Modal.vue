<template>
  <div class="backdrop" v-on:click.self="closeModal">
    <div class="box">
      <h2>Modal Box</h2>
      <h3>{{ title }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  data() {
    return {};
  },
  props: {
    title: String,
  },
  methods: {
    closeModal() {
      this.$emit("close");
    },
  },
};
</script>

<style scoped>
.box {
  padding: 20px;
  margin: 20px auto;
  width: 500px;
  border-radius: 10px;
  background: white;
}

.backdrop {
  top: 10%;
  right: 1vw;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 50%;
  height: 600px;
}
</style>
