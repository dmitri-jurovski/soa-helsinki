<template>
	
			 
	
			 <b-card 
          :img-src="instmedialistitem.images.low_resolution.url"
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