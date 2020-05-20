<template>
  <div>
    <!-- Navigation -->
    <Navigation />
    <!-- Header -->
    <Header v-if="!$store.state.posts.title" />
    <!-- Content -->
    <b-container class="mt-2 mb-2">
      <!-- Content -->
      <nuxt />
    </b-container>
    <!-- Footer -->
    <Footer />
  </div>
</template>

<script>
import Navigation from '~/components/navigation/index.vue'
import Header from '~/components/header.vue'
import Footer from '~/components/footer.vue'

export default {
  components: {
    Navigation, Header, Footer
  }
}
</script>
