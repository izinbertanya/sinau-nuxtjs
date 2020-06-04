<template>
  <b-navbar-brand :href="link">
    <img :src="src" :alt="alt">
  </b-navbar-brand>
</template>

<script>
export default {
  props: {
    link: {
      type: String,
      default: '#'
    },
    src: {
      type: String,
      default: 'https://dummyimage.com/214x59/206de0/ffffff'
    },
    alt: {
      type: String,
      default: 'Logo'
    }
  }
}
</script>

<style>

</style>
