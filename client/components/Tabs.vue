<template>
  <ul>
    <li v-for="item in items" :key="item.index">{{ item }}</li>
  </ul>
</template>

<script>
export default {
  name: 'Tabs',
  props: {
    items: Array
  },
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
ul {
  display: inline;
  margin: 0 48px;
  padding: 0;
  list-style-type: none;

  li {
    display: inline;
    margin: 16px;
    color: grey;
    font-size: 14px;

    &::before {
      content: '#';
    }
  }
}
</style>
