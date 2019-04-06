<template>
  <header>
    <i class="material-icons" @click="open">menu</i>
    <Logo class="logo"/>
    <div class="spacer"></div>
    <Tabs class="tabs" :items="tags"/>
    <i class="material-icons">search</i>
    <NavigationDrawer ref="drawer"/>
  </header>
</template>

<script>
export default {
  name: 'TheHeader'
}
</script>
