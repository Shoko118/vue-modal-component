<template>
  <div class="text-center pt-2">
    <button
      @click="falseVisible = true"
      class="bg-pink-400 py-2 px-3 text-white rounded-xl text-xl"
    >
      Open Modal {{ falseVisible }}
    </button>
    <Modal :trueVisible="falseVisible" @close="falseVisible = false" />
  </div>
</template>

<script>
import { ref } from "vue";
import Modal from "../components/Modal.vue";
export default {
  setup() {
    const falseVisible = ref(false);
    return {
      falseVisible,
    };
  },
  components: { Modal },
};
</script>
