<template>
  <h1>{{ title }}</h1>

  <button @click="toggleModal">Toggle Modal</button>
  <p>some text</p>
  <div v-if="showModal">
    <ModalVue
      :modalTitle="modalTitle"
      :content="modalContent"
      :theme="theme"
      @close="toggleModal"
    />
  </div>
</template>

<script>
import ModalVue from "./components/Modal.vue";

export default {
  //showModal: true,
  name: "App",
  components: { ModalVue },
  data() {
    return {
      title: "My First Vue app :)",
      modalTitle: "Here is tha modal title",
      modalContent: "This   is content of the modal",
      theme: "sale",
      showModal: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
  },
};
//https://www.youtube.com/watch?v=KM1U6DqZf8M&list=PL4cUxeGkcC9hYYGbV60Vq3IXYNfDk8At1&index=5&ab_channel=TheNetNinja
</script>
<style></style>
