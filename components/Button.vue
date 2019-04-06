<template>
  <button>{{ text }}</button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="less" scoped>
button {
  margin: 4px;
  padding: 8px;
  background-color: transparent;
  border: none;
  color: #222;

  &:active {
  }

  &:hover {
    background-color: darken(#fff, 4);
  }
}
</style>
