<template>
  <header>
    <i class="material-icons">menu</i>
    <span class="logo">Phoenix</span>
    <div class="spacer"></div>
    <Tabs class="tabs" :items="tags"/>
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
      tags: tags.slice(0, 8)
    }
  }
}
</script>

<style lang="scss" scoped>
@import './assets/style/vars';

header {
  display: flex;
  padding: 48px;
  align-items: center;

  @media #{$small-viweport} {
    padding: 16px;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 48px;
    font-size: 24px;
    font-weight: 700;

    @media #{$small-viweport} {
      margin: 0 16px;
    }
  }

  .spacer {
    flex: 1;
  }

  .tabs {
    overflow: hidden;

    @media #{$small-viweport} {
      order: 1;
      margin: 24px 0 0;
      overflow: auto;
    }
  }
}
</style>

