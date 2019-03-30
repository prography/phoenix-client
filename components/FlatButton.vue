<template>
  <button>{{ text }}</button>
</template>

<script>
export default {
  name: 'FlatButton',
  props: {
    text: String
  }
}
</script>

<style lang="scss" scoped>
@import './assets/style/vars';

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
