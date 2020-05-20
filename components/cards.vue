<template>
  <b-card @click="openDetail(detail)">
    <img class="card-img-top" :src="img" alt="Card image cap">
    <b-card-body>
      <b-card-text>
        <small class="text-muted">{{ author }} - {{ source }}</small>
      </b-card-text>
      <b-card-title>{{ title }}</b-card-title>
      <b-card-text>
        <small class="text-muted">{{ publishedAt }}</small>
      </b-card-text>
      <btnYellow>Selengkapnya</btnYellow>
    </b-card-body>
  </b-card>
</template>

<script>
import btnYellow from '~/components/button/yellow.vue'

export default {
  components: {
    btnYellow
  },
  props: {
    img: {
      type: String,
      default: null
    },
    author: {
      type: String,
      default: null
    },
    source: {
      type: String,
      default: null
    },
    title: {
      type: String,
      default: null
    },
    publishedAt: {
      type: String,
      default: null
    },
    detail: {
      type: Object,
      default: null
    }
  },
  methods: {
    openDetail (data) {
      this.$store.commit('SET_POSTS', data)
      this.$router.replace({ path: '/detail' })
    }
  }
}
</script>

<style>

</style>
