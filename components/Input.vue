<template>
  <div class="input-wrapper">
    <input type="text" v-model="value" :placeholder="placeholder">
  </div>
</template>

<script>
export default {
  name: 'Input',
  props: {
    placeholder: String,
    value: String
  },
  watch: {
  }
}
</script>

<style lang="scss" scoped>
@import './assets/style/vars';

input {
  width: 100%;
  margin: 4px 0;
  padding: 4px;
  border: 2px #eee solid;
  border-radius: 4px;
}
</style>
