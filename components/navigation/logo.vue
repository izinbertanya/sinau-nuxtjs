<template>
  <b-navbar-brand :href="link">
    <img :src="src" :alt="alt">
  </b-navbar-brand>
</template>

<script>
export default {
  data () {
    return {
      link: '#',
      src: 'https://dummyimage.com/214x59/206de0/ffffff',
      alt: 'Ini Logo'
    }
  }
}
</script>

<style>

</style>
