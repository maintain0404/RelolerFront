<template>
  <b-navbar
    fixed-top
    type="is-light">
    <template slot="brand">
      <b-navbar-item a="#">
        ReLOL
      </b-navbar-item>
    </template>
    <template slot="start">
      <b-navbar-item>
        <Search v-if="is_main"></Search>  
      </b-navbar-item>
    </template>
    <template slot="end">
      <b-navbar-item v-if="is_signin" tag="div">
        <b-skeleton circle>
        </b-skeleton>
        <b-skeleton>
        </b-skeleton>
      </b-navbar-item>
      <b-navbar-item v-else tag="div">
        <div class="buttons">
          <a class="button is-primary">
            <strong>Sign Up</strong>
          </a>
          <a class="button is-light">
            Sign In
          </a>
        </div>
      </b-navbar-item>
    </template>
  </b-navbar>        
</template>

<script>
import Vue from 'vue'
import { Navbar } from 'buefy'
import Search from './Search.vue'

Vue.use(Navbar)
Vue.use(Search)

export default {
  name: 'NavHeader',
  props: {
    is_main: {
      type: Boolean,
      default: false
    },
    is_signin: {
      type: Boolean,
      default: false
    }
  },
  components: {
    Search
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
