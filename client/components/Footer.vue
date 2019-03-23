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
footer {
  padding: 1.5rem 3rem;
  background-color: #ff6f61;
  color: white;

  .team-name {
    font-weight: 700;
  }
}
</style>
