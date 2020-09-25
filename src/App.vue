<template>
  <div id="app">
    <NavHeader v-bind:is_main="true"></NavHeader>
    <div class="container">
      <div id="user-info">
      </div>
      <div id="matchs-info">
        <Match></Match>
      </div>
    </div>
  </div>
</template>

<script>
import NavHeader from './components/NavHeader.vue'
import Match from './components/Match.vue'

export default {
  name: 'App',
  components: {
    NavHeader,
    Match
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
#search{
  height:52px;
  width:700px;
}
.main-box{
  width:100%;
  height:100%;
  display:flex;
  flex-direction: column;
}
.main-inner{
  align-items:center;
}
</style>
