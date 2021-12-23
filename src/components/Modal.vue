<template>
  <div
    v-if="trueVisible"
    class="bg-gray-300 min-h-screen fixed inset-0 bg-opacity-60"
  >
    <div class="bg-white shadow-lg rounded-lg w-5/12 h-2/5 mt-14 mx-auto">
      <button
        @click="$emit('close')"
        class="bg-green-500 py-1 px-3 rounded-xl mt-24"
      >
        Close modal
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    trueVisible: {
      type: Boolean,
      required: true,
    },
  },
  setup() {
    return {};
  },
};
</script>
