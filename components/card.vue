<template>
  <b-card>
    <!-- <b-card @click="clickaction"> -->
    <img class="card-img-top" :src="img" alt="Card image cap">
    <b-card-body>
      <slot />
    </b-card-body>
  </b-card>
</template>

<script>
export default {
  props: {
    img: {
      type: String,
      default: ''
    }
    // clickaction: { type: Function, default: () => '' }
  }
}
</script>

<style>

</style>
