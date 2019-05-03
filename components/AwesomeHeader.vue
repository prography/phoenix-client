<template>
  <header>
    <v-toolbar fixed app flat>
      <v-toolbar-side-icon @click="drawer = !drawer"/>
      <v-toolbar-title>
        <nuxt-link to="/">
          <logo font-size="16px"/>
        </nuxt-link>
      </v-toolbar-title>
    </v-toolbar>
    <v-navigation-drawer v-model="drawer" fixed app>
      <v-list>
        <v-list-tile v-for="(item, i) in items" :key="i" :to="item.to" router exact>
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title"/>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
  </header>
</template>

<script>
import Logo from '@/components/Logo'

export default {
  name: 'AwesomeHeader',
  components: {
    Logo
  },
  data() {
    return {
      drawer: false,
      items: [
        {
          icon: 'apps',
          title: 'Welcome',
          to: '/'
        }
      ]
    }
  }
}
</script>
