<template>
	<div class="riot-id-info">
		<div class="riot-id-profile">
			<div class="lol-icon">
				<b-skeleton width="200px" height="200px"></b-skeleton>
			</div>
			<div class="lol-tier">
				<b-skeleton width="200px" height="100px"></b-skeleton>
			</div>
		</div>
		<div class="riot-id-logs">
			<div class="lol-nickname">
				<b-skeleton></b-skeleton>
			</div>
			<div class="lol-logs">
				<b-skeleton></b-skeleton>
			</div>
		</div>
	</div>
</template>

<script>
import Vue from 'vue'
import { Skeleton } from 'buefy'

Vue.use(Skeleton)

export default {
	name: "RiotIdInfo"
}
</script>

<style>
.riot-id-info{
	display: flex;
	flex-direction: row;
	margin-bottom: 20px;
}
.riot-id-profile{
	width:200px;
	margin-right:20px;
	flex-grow: 0;
	flex-shrink: 0;
	display: flex;
	flex-direction: column;
}
.riot-id-logs{
	flex-grow: 1;
	flex-shrink: 1;
	display: flex;
	flex-direction: column;
}
.lol-icon{
	margin-bottom:10px;
}
.lol-nickname{
	margin-bottom:10px;
	flex-basis: 60px;
	flex-shrink: 0;
	flex-grow: 0;
	margin-bottom:10px;
}
.lol-logs{
	flex-shrink:1;
	flex-grow:1;
}
</style>