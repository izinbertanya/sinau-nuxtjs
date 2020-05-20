<template>
  <div class="mt-5">
    <b-row>
      <div class="card-columns">
        <Card
          v-for="item in posts.slice(0,current)"
          :key="item.key"
          :img="item.urlToImage"
          :title="item.title"
          :author="item.author"
          :source="item.source.name"
          :published-at="item.publishedAt"
          :detail="item"
        />
      </div>
    </b-row>
    <div @click="loadMore()">
      <btnYellow class="btn-more" size="lg">
        Load More
      </btnYellow>
    </div>
  </div>
</template>

<script>
import btnYellow from '~/components/button/yellow.vue'
import Card from '~/components/card.vue'

export default {
  components: {
    Card, btnYellow
  },
  async asyncData (context) {
    const response = await context.$axios.get('/everything?q=programming&domains=techcrunch.com,techinasia.com&apiKey=afb43233e81b4e63985ff02a3a313d45')
    const posts = response.data.articles
    return {
      posts,
      current: 9
    }
  },
  methods: {
    loadMore () {
      this.current += 9
    }
  },
  head: {
    title: 'Ini Blog'
  }
}
</script>

<style lang="scss" scoped>
/*
 * Card Columns Masonry - Bootstrap 4
 * https://codepen.io/JacobLett/pen/oZmWdd
 */
/* Medium devices (tablets, 768px and up) The navbar toggle appears at this breakpoint */
@media (min-width: 768px) {
  .card-columns {column-count: 3;}
}
/* Large devices (desktops, 992px and up) */
@media (min-width: 992px) {
 .card-columns {column-count: 3;}
}

/* Extra large devices (large desktops, 1200px and up) */
@media (min-width: 1200px) {
   .card-columns {column-count: 3;}
}
.btn-more {
  margin: 20px auto;
  display: block;
}
</style>
