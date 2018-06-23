<template>


 	<b-container>
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