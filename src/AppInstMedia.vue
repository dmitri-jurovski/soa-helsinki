<template>
	<b-container class="pt-5">
		<b-card-group columns>

			<inst-media-item 
				v-for="(item, i) in instmedialist"
			    :instmedialistitem="item"
			    v-bind:key="i"
			/>
	
		</b-card-group>
	</b-container>
</template>

<script>
import AppInstMediaItem from './AppInstMediaItem.vue';

	export default {
  		name: 'InstMedia',
  		props: ['instmedialist'],
  		components: {
  			'inst-media-item': AppInstMediaItem
  		},// components
  	}// export
</script>


<style lang="scss">
	

@media (min-width: 576px) { 
	.card-columns {
    	column-count: 2;
	}
}
@media (min-width: 768px) { 
	.card-columns {
    	column-count: 3;
	}
}
@media (min-width: 992px) { 
	.card-columns {
    	column-count: 4;
	}
}


</style>















