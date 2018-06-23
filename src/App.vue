<template>
  <div>
    
<app-header
  
></app-header>

<inst-media
  :instmedialist = 'media'
/>


    
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://gitter.im/vuejs/vue" target="_blank">Gitter Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
import AppHeader from './AppHeader.vue';
import AppInstMedia from './AppInstMedia.vue';

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
#navbarHeader {
  max-height: 100vw;
    overflow: hidden;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
