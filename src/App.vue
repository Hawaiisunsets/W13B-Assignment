<template>
  <div id="app">
    <TweetList/>

  </div>
</template>

<script>
import TweetList from '@/components/TweetList.vue';



export default {
  name: 'App',
  components: {
    TweetList,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

