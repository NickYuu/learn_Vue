<template>
  <div>
    <h2>this is profile</h2>
    <h3>{{$route.query}}</h3>
  </div>
</template>

<script>
  export default {
    name: "Profile",
    created() {
      console.log('created')
    },
    destroyed() {
      console.log('destroyed')
    }
  }
</script>

<style scoped>

</style>