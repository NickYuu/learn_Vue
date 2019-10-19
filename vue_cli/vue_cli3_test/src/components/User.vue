<template>
  <div>
  <h2>this is user</h2>
  <h3>UserID: {{userId}}</h3>
  </div>
</template>

<script>
  export default {
    name: "User",
    computed: {
      userId() {
        return this.$route.params.userId
      }
    }
  }
</script>

<style scoped>

</style>