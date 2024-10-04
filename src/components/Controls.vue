<template>
  <div class="controls">
    <button
      v-for="(enabled, index) in visibility"
      :key="index"
      @click="emitToggle(index)"
      :class="['control-button', enabled ? 'enabled' : 'disabled']"
    ></button>
  </div>
</template>

<script>
export default {
  name: "Controls",
  props: {
    visibility: Array,
  },
  methods: {
    emitToggle(index) {
      this.$emit("toggleVisibility", index);
    },
  },
};
</script>

<style scoped lang="scss">
.controls {
  margin-bottom: 20px;
}
.control {
  &-button {
    width: 20px;
    height: 20px;
    margin: 0 5px;
    background-color: black;
    border: 1px solid black;
    cursor: pointer;
    transition: all 0.3s ease;
    &:hover {
      transform: scale(1.1);
    }
    &.enabled {
      background-color: black;
      border-color: black;
    }
    &.disabled {
      background-color: transparent;
      border-color: black;
    }
  }
}
</style>
