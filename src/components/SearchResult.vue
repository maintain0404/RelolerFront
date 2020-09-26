<template>
  <section>
		<div class="container">
			<div id="user-info">
				<RiotIdInfo></RiotIdInfo>
			</div>
			<div id="matchs-info">
				<Match></Match>
			</div>
		</div>
	</section>
</template>

<script>
import Match from './Match.vue'
import RiotIdInfo from './RiotIdInfo.vue'

export default {
	name: 'SearchResult',
	components:{
		RiotIdInfo,
		Match
	}
}
</script>