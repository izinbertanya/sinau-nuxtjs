<template>
  <div class="detail">
    <b-container>
      <b-row class="justify-content-md-center">
        <b-col cols="8">
          <img :src="posts.urlToImage" alt="Card image cap" class="img-fluid">
          <b-card-text><small class="text-muted">{{ posts.publishedAt }} - {{ posts.author }} - {{ posts.source.name }}</small></b-card-text>
          <b-card-title>{{ posts.title }}</b-card-title>
          <b-card-text>{{ posts.description }}</b-card-text>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  computed: {
    posts () { return this.$store.state.posts }
  },
  head () {
    return {
      title: this.posts.title
    }
  }
}
</script>

<style lang="scss" scoped>
.detail {
  padding-top: 5rem;
  padding-bottom: 2rem;
}
</style>
