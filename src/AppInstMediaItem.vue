<template>
	<div>
			 <img v-bind:src="instmedialistitem.images.low_resolution.url">
			<p>Test</p> 
	</div>
</template>

<script>
console.log("test log");
	export default {
      name: 'InstMediaItem',
      props: ['instmedialistitem'],
  }
</script>