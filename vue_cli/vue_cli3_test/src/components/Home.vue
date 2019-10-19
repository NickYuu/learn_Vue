<template>
  <div>
    <h2>this is home</h2>
    <router-link to="/home/news" tag="button" replace >News</router-link>
    <router-link to="/home/message" tag="button" replace >Msg</router-link>
    <router-view></router-view>
  </div>
</template>

<script>
  export default {
    name: "Home",
    data() {
      return {
        path: '/home/news'
      }
    },
    created() {
      console.log('created')
    },
    destroyed() {
      console.log('destroyed')
    },
    activated() {
      this.$router.push(this.path).catch(err => {})
    },
    beforeRouteLeave(to, from, next) {
      this.path = from.path
      next()
    }
  }
</script>

<style scoped>

</style>