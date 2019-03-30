<template>
  <footer>
    <span>
      &copy; 2019&nbsp;<a class="team-name"><Logo fontColor="white" fontSize="12px"/>&nbsp;in Prography</a>. All rights reserved.
    </span>
  </footer>
</template>

<script>
import Logo from '@/components/Logo.vue'

export default {
  name: 'Footer',
  components: {
    Logo
  }
}
</script>

<style lang="scss" scoped>
@import './assets/style/vars';

footer {
  padding: 24px 48px;
  background-color: $primary-color;
  color: white;
  font-size: 14px;

  @media #{$small-viweport} {
    padding: 24px;
  }

  .team-name {
    font-weight: 700;
  }
}
</style>
