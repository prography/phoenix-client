<template>
  <main>
    <header class="logo-wrapper">
      <Logo font-size="56px"/>
    </header>
    <section class="card">
      <nuxt/>
    </section>
    <footer>
      <Copyright/>
    </footer>
  </main>
</template>

<script>
import Copyright from '@/components/Copyright.vue'
import Logo from '@/components/Logo.vue'

export default {
  components: {
    Copyright,
    Logo
  }
}
</script>

<style lang="less">
body {
  background-color: #eee;
}
</style>

<style lang="less" scoped>
main {
  max-width: 600px;
  margin: 0 auto;

  .logo-wrapper {
    margin: 0 auto;
    padding: 64px 0 32px;
    text-align: center;
  }

  .card {
    margin: 0 8px;
    padding: 32px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.2);
  }

  footer {
    margin: 16px 0;
    text-align: center;
  }
}
</style>
