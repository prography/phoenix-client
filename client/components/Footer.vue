<template>
  <footer>
    <span>
      &copy; 2019
      <a class="team-name">Phoenix in Prography</a>. All rights reserved.
    </span>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss" scoped>
@import './assets/style/vars';

footer {
  padding: 24px 48px;
  background-color: #ff6f61;
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
