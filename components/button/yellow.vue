<template>
  <b-button :pill="pill" variant="warning" :size="size">
    <slot />
  </b-button>
</template>

<script>
export default {
  props: {
    size: {
      type: String,
      default: ''
    },
    pill: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style>
.btn-warning {
    background-color: #FFCA0D;
    font-weight: bold;
}
</style>
