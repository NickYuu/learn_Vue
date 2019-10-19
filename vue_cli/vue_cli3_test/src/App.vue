<template>
  <div id="app">
    <h2>APP</h2>
    <!--    <h3><router-link to="/home" tag="button" replace active-class="active">Home</router-link></h3>-->
    <!--    <h3><router-link to="/about" tag="button" replace active-class="active">About</router-link></h3>-->
    <!--    <h3><router-link to="/home" tag="button" replace>Home</router-link></h3>-->
    <!--    <h3><router-link to="/about" tag="button" replace>About</router-link></h3>-->
    <!--    <button @click="homeClick">Home</button>-->
    <!--    <button @click="aboutClick">About</button>-->
    <router-link to="/home" tag="button" replace>Home</router-link>
    <router-link to="/about" tag="button" replace>About</router-link>
    <router-link :to="'/user/' + userId" tag="button" replace>User</router-link>
    <router-link :to="{path: '/profile', query: {first_name: 'Nick', last_name:'Yu'}}" tag="button" replace>Profile</router-link>
    <keep-alive exclude="Profile,User">
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>

  export default {
    name: 'app',
    data() {
      return {
        userId: 'r1d234'
      }
    },
    methods: {
      // homeClick() {
      //   this.$router.replace('/home')
      // },
      // aboutClick() {
      //   this.$router.replace('/about')
      // }
    }
  }
</script>

<style>
  .active {
    color: red;
  }
</style>
