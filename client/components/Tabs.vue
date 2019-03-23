<template>
  <ul class="tabs">
    <li v-for="item in items" :key="item.index" class="tab">{{ item }}</li>
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
  padding: 2rem;
  list-style-type: none;

  li {
    display: inline;
    margin: 1rem;
    color: grey;

    &::before {
      content: '#';
    }
  }
}
</style>
