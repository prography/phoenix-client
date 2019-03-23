<template>
  <div class="card">
    <img src="https://picsum.photos/400" alt="Thumbnail">
    <div class="content">
      <h4>{{ title }}</h4>
      <p>content</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props: {
    title: String
  }
}
</script>

<style lang="scss" scoped>
.card {
  background-color: white;
  border: #eee 1px solid;

  img {
    width: 100%;
    height: auto;
  }

  .content {
    margin: 1rem;

    h4 {
      margin: 0;
      font-size: 24px;
    }

    p {
      font-size: 14px;
    }
  }
}
</style>
