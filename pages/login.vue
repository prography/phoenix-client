<template>
  <v-layout align-center justify-center>
    <v-flex xs12 sm6>
      <div class="logo-wrapper">
        <nuxt-link to="/">
          <logo font-size="56px"/>
        </nuxt-link>
      </div>
      <v-card class="px-3 pt-3">
        <v-card-title class="headline pb-0">Login</v-card-title>
        <v-card-text class="text-xs-right">
          <v-text-field type="email" label="Email"/>
          <v-text-field type="password" label="Password"/>
          <nuxt-link to="forgot">forgot password?</nuxt-link>
          <br>
          <br>
          <v-btn block flat href="/signup">Create New Accout</v-btn>
          <v-btn color="primary" block flat>Login</v-btn>
        </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '@/components/Logo'

export default {
  layout: 'empty',
  components: {
    Logo
  }
}
</script>

<style scoped>
.logo-wrapper {
  margin: 0 auto;
  padding: 64px 0 32px;
  text-align: center;
}
</style>
