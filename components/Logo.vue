<template>
  <span :style="{ fontSize }">Phoenix</span>
</template>

<script>
export default {
  name: 'Logo',
  props: {
    fontSize: String
  }
}
</script>

<style lang="scss" scoped>
span {
  font-weight: 700;
}
</style>

