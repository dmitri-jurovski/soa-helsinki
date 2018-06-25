<template>
  <div>

    <app-header></app-header>

    <inst-media :instmedialist = 'media'/>
    
    <footer>
      <p>Sight on Art from Helsinki.</p>
    </footer>

  </div>
</template>


<script>
// Import Components
import AppHeader from './AppHeader.vue';
import AppInstMedia from './AppInstMedia.vue';

// Instargem account access by token
const token = '7562922180.1677ed0.fc4e273eea1049be86e4a335cb642dbc';
const insUrl = 'https://api.instagram.com/v1/users/self/media/recent/?access_token=' + token;


export default {
  name: 'instApp',
  data () {
    return {
      title: 'soa helsinki',
      media: []
    }
  },

  components: {
    'app-header': AppHeader,
    'inst-media': AppInstMedia
  },

  methods: {
    sayLog: function(){
      console.log("$vm.transitioning");
    },
  }, // methods

  created: function () {
      axios.get(insUrl)
      .then(response => {
        // JSON responses are automatically parsed.
        this.media = response.data.data;

        // this.media.forEach(function (currentValue, index, array) {
        //     Vue.set(array[index],  'viewMode',  false );
        //     console.log("This media", this.media);
        // });
        
      })
      .catch(error => console.log(error))

    }
}
</script>

<style lang="scss">

body {
  background: #f5f5f5;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;


  
}


</style>
