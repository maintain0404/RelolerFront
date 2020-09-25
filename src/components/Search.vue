<template>
  <div class="search-box">
    <div class="search-input">
      <b-input v-model="summoner_name"
        type="is-primary"
      >
      </b-input>
    </div>
    <div class="search-button">
      <b-button 
        type="is-primary"
      >
        Search
      </b-button>
    </div>
  </div>

</template>

<script>
import Vue from 'vue'
import { Input, Field, Button } from 'buefy'

Vue.use(Input)
Vue.use(Field)
Vue.use(Button)

export default {
  name: 'Search',
  data: function(){
    return {
      summoner_name: "소환사명을 입력하세요"
    }
  },
}
</script>

<style>
.search-box{
  display:flex;
  flex-direction: row;
}
.search-input{
  flex-grow:1;
  padding:0.2em;
}
.search-button{
  flex-grow:0;
  padding:0.2em;
}
</style>

