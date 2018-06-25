<template>
	
			 
	
<b-card overlay
		img-fluid
        :img-src="instmedialistitem.images.standard_resolution.url"
      	img-alt="Image"
      	img-top
      	tag="article"
      	class=" box-shadow">
    <p class="card-text">{{ instmedialistitem.caption.text }}</p>
    
  </b-card>

</template>

<script>
console.log("test log");
	export default {
      name: 'InstMediaItem',
      props: ['instmedialistitem'],

  }

</script>

<style lang="scss">
	
</style>