<template>
	<div class='maincontainer'>
		<div class="mainlogo">
			<img :src="require('@/assets/challenger.png')">
		</div>
		<div class="searchwrapper">
			<Search></Search>
		</div>
  </div>
</template>

<script>
import Vue from 'vue'
import Search from './Search.vue'

Vue.use(Search)
export default {
	name: "Main",
	components:{
		Search
	}	
}
</script>

<style scoped>
.maincontainer{
	display:flex;
	flex-direction:column;
	justify-content: center;
	align-items: center;
}
.mainlogo{
	margin-top:80px;
}
.searchwrapper{
	width:500px;
}
</style>