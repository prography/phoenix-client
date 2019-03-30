<template>
  <main>
    <Logo class="logo" fontSize="60px"/>
    <FormCard>
      <h1>Login</h1>
      <Input placeholder="ID"/>
      <Input placeholder="Password"/>
      <div class="buttons">
        <FlatButton text="Create New Accout"/>
        <FlatButton text="Login"/>
      </div>
    </FormCard>
  </main>
</template>

<script>
import FlatButton from '@/components/FlatButton.vue'
import FormCard from '@/components/FormCard.vue'
import Input from '@/components/Input.vue'
import Logo from '@/components/Logo.vue'

export default {
  components: {
    FlatButton,
    FormCard,
    Input,
    Logo
  },
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
@import './assets/style/vars';

main {
  height: 100vh;
  background-color: #eee;

  h1 {
    margin-block-start: 0;
  }

  .logo {
    display: block;
    padding: 64px 0 32px;
    text-align: center;
  }

  .buttons {
    display: grid;
    grid-template-columns: repeat(2, 50%);

    @media #{$small-viweport} {
      grid-template-columns: 100%;
    }
  }
}
</style>
