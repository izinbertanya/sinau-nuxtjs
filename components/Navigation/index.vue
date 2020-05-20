<template>
  <div>
    <b-navbar toggleable="lg" fixed="top">
      <b-container v-if="!$store.state.posts.title">
        <Logo />
        <b-navbar-toggle target="nav-collapse" />
        <b-collapse id="nav-collapse" is-nav>
          <Menu />
        </b-collapse>
      </b-container>
      <b-container v-else>
        <a href="#" class="navbar-brand" @click="goBack()">
          Back
        </a>
      </b-container>
    </b-navbar>
  </div>
</template>

<script>
import Logo from '~/components/navigation/logo.vue'
import Menu from '~/components/navigation/menu.vue'

export default {
  components: {
    Logo, Menu
  },
  methods: {
    goBack () {
      this.$store.commit('SET_POSTS', [])
      this.$router.replace({ path: '/' })
    }
  }
}
</script>

<style lang="scss" scoped>
.navbar {
  background-color: white;
  box-shadow: 0px -9px 20px #000000;

  .nav {
    &-item {
    padding: 0 .5rem;
    }
    &-link {
    padding: 1rem;
    color: #888888;
    }
  }
}
</style>
