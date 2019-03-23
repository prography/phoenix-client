<template>
  <header>
    <i class="material-icons">menu</i>
    <span class="logo">Phoenix</span>
    <div class="spacer"></div>
    <Tabs :items="tags"/>
    <i class="material-icons">search</i>
  </header>
</template>

<script>
import Tabs from '@/components/Tabs.vue'

import tags from '@/assets/data/tempTags'

export default {
  name: 'Header',
  components: {
    Tabs
  },
  data() {
    return {
      tags: tags.slice(0, 5)
    }
  }
}
</script>

<style lang="scss" scoped>
header {
  display: flex;
  padding: 0 3rem;
  height: 5rem;
  align-items: center;

  .logo {
    margin: 0 3rem;
    font-size: 2rem;
    font-weight: 700;
  }

  .spacer {
    flex: 1;
  }
}
</style>

