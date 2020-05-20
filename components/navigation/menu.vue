<template>
  <b-navbar-nav>
    <b-nav-item v-for="menu in menus" :key="menu.id" :href="menu.link" :active="menu.status">
      {{ menu.name }}
    </b-nav-item>
  </b-navbar-nav>
</template>

<script>
export default {
  data () {
    return {
      menus: [{
        id: 1,
        name: 'Home',
        link: '#',
        status: true
      }, {
        id: 2,
        name: 'Blog',
        link: '#',
        status: false
      }, {
        id: 3,
        name: 'About',
        link: '#',
        status: false
      }]
    }
  }
}
</script>

<style>

</style>
