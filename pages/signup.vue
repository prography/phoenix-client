<template>
  <article>
    <h1>Sign Up</h1>
    <InputText placeholder="Email"/>
    <InputText placeholder="Password"/>
    <div class="buttons">
      <Button text="Create an Accout"/>
      <Button text="or, Login"/>
    </div>
  </article>
</template>

<script>
import Button from '@/components/Button.vue'
import InputText from '@/components/InputText.vue'

export default {
  layout: 'card',
  components: {
    Button,
    InputText
  }
}
</script>

<style lang="less" scoped>
.buttons {
}
</style>
