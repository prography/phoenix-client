<template>
  <section class="container">
    <div class="card">
      <slot/>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FormCard'
}
</script>

<style lang="scss" scoped>
.container {
  max-width: 576px;
  margin: 0 auto;
}

.card {
  margin: 0 8px;
  padding: 32px;
  background-color: white;
  border-radius: 8px;
  box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.2);
}
</style>
