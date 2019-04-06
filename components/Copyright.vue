<template>
  <span :style="{ color: fontColor, fontSize }">
    &copy;2019&nbsp;<b>Phoenix</b>&nbsp;in <b>Prography</b>. All rights reserved.
  </span>
</template>

<script>
export default {
  name: 'Copyright',
  props: {
    fontColor: {
      type: String,
      default: '#212121'
    },
    fontSize: {
      type: String,
      default: '14px'
    }
  }
}
</script>
