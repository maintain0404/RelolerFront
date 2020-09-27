<template>
  <div id="app">
    <NavHeader v-bind:is_main="is_navbar_search"></NavHeader>
    <router-view></router-view>
  </div>
</template>

<script>
import Vue from 'vue'
import Buefy from 'buefy'
import NavHeader from './components/NavHeader.vue'
import SearchResult from './components/SearchResult.vue'
import Main from './components/Main.vue'
import VueRouter from 'vue-router'

Vue.use(VueRouter)
Vue.config.productionTip = false
Vue.use(Buefy)

const router = new VueRouter({
  routes: [
    { 
      path: '/',
      component: Main
    },{
      path: '/result',
      component: SearchResult
    }
  ]
})


export default {
  name: 'App',
  data: function(){
    return {
      is_navbar_search: false
    }
  },
  watch:{
    $route: function(to){
      if(to.path == '/result' ){
        this.is_navbar_search = true;
      }
      else if(to.path == '/'){
        this.is_navbar_search = false;
      }
    }
  },
  components: {
    NavHeader
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
