<template>
  <footer>
    <Copyright fontColor="white"/>
  </footer>
</template>

<script>
import Copyright from '@/components/Copyright.vue'
import Logo from '@/components/Logo.vue'

export default {
  name: 'TheFooter',
  components: {
    Copyright,
    Logo
  }
}
</script>

<style lang="less" scoped>
@import '~assets/vars';

footer {
  padding: 24px 48px;
  background-color: @footer-color;

  @media @small {
    padding: 24px;
  }
}
</style>
