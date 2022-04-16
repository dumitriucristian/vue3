<template>
  <div class="backdrop" @click.self="closeModal">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <h1>{{ modalTitle }}</h1>
      <p>{{ content }}</p>
    </div>
  </div>
</template>

<script scope>
export default {
  props: ["modalTitle", "content", "theme", "showModal"],
  methods: {
    closeModal() {
      console.log("ssss");
      this.$emit("close");
    },
  },
};
</script>
<style>
.backdrop {
  width: 100%;
  height: 100%;
  background-color: rgba(128, 128, 128, 0.205);
  position: fixed;
  top: 0;
}

.modal {
  width: 400px;
  height: 200px;
  border: solid 1px;
  background-color: white;
  border-radius: 10px;
  margin: 100px auto;
}
.sale {
  background-color: green;
  color: white;
}
</style>
