<template>
  <div>
    <!-- Navigation -->
    <Navigation :menus="menus" />
    <!-- Header -->
    <Header v-if="!$store.state.posts.title" />
    <!-- Content -->
    <b-container class="mt-2 mb-2">
      <!-- Content -->
      <nuxt />
    </b-container>
    <!-- Footer -->
    <Footer>
      Ini Footer
    </Footer>
  </div>
</template>

<script>
import Navigation from '~/components/navigation/index.vue'
import Header from '~/components/header.vue'
import Footer from '~/components/footer.vue'

export default {
  components: {
    Navigation, Header, Footer
  },
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
