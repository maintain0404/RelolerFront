<template>
  <div id="app">
    <NavHeader v-bind:is_main="true"></NavHeader>
    <router-view></router-view>
  </div>
</template>

<script>
import Vue from 'vue'
import Buefy from 'buefy'
import NavHeader from './components/NavHeader.vue'
import SearchResult from './components/SearchResult.vue'
import Search from './components/Search.vue'
import VueRouter from 'vue-router'

Vue.use(VueRouter)
Vue.config.productionTip = false
Vue.use(Buefy)

const routes = [
  { 
    path: '/',
    component: Search
  },{
    path: '/result',
    component: SearchResult
  }
]

const router = new VueRouter({
  routes
})


export default {
  name: 'App',
  components: {
    NavHeader,
  },
  router
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
