<template>
  <div class="backdrop" @click.self="closeModal">
    <div class="modal">
      <slot>We need some content, bro!</slot>
      <div class="actions">
        <slot name="links">We need some action, bro!</slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["header", "text"],
  data() {
    return {};
  },
  methods: {
    closeModal() {
      this.$emit("closeModal");
    },
  },
};
</script>

<style>
.modal {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: white;
  border-radius: 10px;
}

.backdrop {
  top: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}
.modal > h1 {
  color: darkolivegreen;
  border: none;
  padding: 0;
}
</style>
