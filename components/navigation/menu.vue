<template>
  <b-navbar-nav>
    <b-nav-item v-for="menu in menus" :key="menu.id" :href="menu.link" :active="menu.status">
      {{ menu.name }}
    </b-nav-item>
  </b-navbar-nav>
</template>

<script>
export default {
  props: {
    menus: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style>

</style>
