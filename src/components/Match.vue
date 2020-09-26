<template>
	<div class="match">
		<div class="columns">
			<div class="column is-two-fifths">
				<div class="columns">
					<div class="column">
						<b-skeleton width="100px" height="100px"></b-skeleton>
					</div>
					<div class="column">
						<b-skeleton circle width="100px" height="100px"></b-skeleton>
					</div>
					<div class="column">
						<b-skeleton width="125px" height="100px"></b-skeleton>
					</div>
				</div>
			</div>
			<div class="column">
				<div class="columns">
					<div class="column is-one-fourth">
						<b-skeleton></b-skeleton>
					</div>
					<div class="column is-one-fourth">
						<b-skeleton></b-skeleton>
					</div>
					<div class="column is-one-fourth">
						<b-skeleton></b-skeleton>
						<b-skeleton></b-skeleton>
						<b-skeleton></b-skeleton>
						<b-skeleton></b-skeleton>
						<b-skeleton></b-skeleton>
					</div>
					<div class="column is-one-fourth">
						<b-skeleton></b-skeleton>
						<b-skeleton></b-skeleton>
						<b-skeleton></b-skeleton>
						<b-skeleton></b-skeleton>
						<b-skeleton></b-skeleton>
					</div>
				</div>	
			</div>
		</div>
	</div>
</template>

<script>
import Vue from 'vue'
import { Skeleton } from 'buefy'

Vue.use(Skeleton)

export default {
	name: "Match"
}
</script>

<style>
.match{
	max-height:50px;
}
</style>