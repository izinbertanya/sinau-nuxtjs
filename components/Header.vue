<template>
  <header class="masthead">
    <b-container class="h-100">
      <b-row class="h-100 align-items-center">
        <b-col cols="12" class="text-center">
          <h1 class="font-weight-light">
            Vertically Centered Masthead Content
          </h1>
          <p class="lead">
            A great starter layout for a landing page
          </p>
        </b-col>
      </b-row>
    </b-container>
  </header>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.masthead {
  height: 100vh;
  min-height: 500px;
  background-image: linear-gradient(to right, rgba(25, 10, 8, 0.64), rgba(124, 35, 28, 0.73)), url('https://source.unsplash.com/AEaTUnvneik/1920x1080');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  color:#FFF;
}
</style>
