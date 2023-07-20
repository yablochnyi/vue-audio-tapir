<template>
  <button v-if="showButton" @click="clickButton" :style="{ 'background-color': color }"
          class="p-3 mt-8 text-black rounded-md">
    {{ label }}
  </button>
</template>

<script>
export default {
  emits: ['submit'],
  props: {
    showButton: {
      type: Boolean,
      default: true
    },
    color: {
      type: String,
    },
    label: {
      type: String,
      default: "Submit"
    }
  },
  methods: {
    clickButton() {
      this.$emit("submit");
    },
  },
};
</script>
