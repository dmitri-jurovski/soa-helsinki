<template>
	<ul class="flashcard-list">
	  <li
	    v-for="(card, i) in instmedialist"
	    v-bind:key="i"
	    >

	    <img v-bind:src="card.images.low_resolution.url" v-bind:alt="card.caption.text" class="fuild-img" />
	  </li>
	</ul>
</template>

<script>
	export default {
  		name: 'InstMedia',
  		props: ['instmedialist']
  	}
</script>