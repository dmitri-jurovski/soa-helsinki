<template>

  <b-navbar sticky toggleable="true" type="dark" variant="purple" style="background-color: #563d7c;">
    <b-container>
      <b-navbar-brand  href="#">soa.Helsinki </b-navbar-brand>
      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      <b-collapse is-nav id="nav_collapse" >
        <b-navbar-nav class="ml-auto">

          <div class="row">
            <div class="col-sm-8 col-md-7 py-4">
              <h4 class="text-white">Sight on Art . Helsinki</h4>
              <p class="text-muted">Add some information about the album below, the author, or any other background context. Make it a few sentences long so folks can pick up some informative tidbits. Then, link them off to some social networking sites or contact information.</p>
            </div>
            <div class="col-sm-4 offset-md-1 py-4">
              <h4 class="text-white">Contact</h4>
              <ul class="list-unstyled">
                <li><a href="#" class="text-white">Follow on Twitter</a></li>
                <li><a href="#" class="text-white">Like on Facebook</a></li>
                <li><a href="#" class="text-white">Email me</a></li>
              </ul>
            </div>
          </div>
        
        </b-navbar-nav>
      
        <b-navbar-nav>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#" disabled>Disabled</b-nav-item>
        </b-navbar-nav>

      </b-collapse>
    </b-container>
  </b-navbar>
</template>

<script>
  export default {
      name: 'AppHeader',
      data () {
        return {

          book: 'Book your personal photo shoot, to keep your memories of your day with a private photo shoot using Helsinki major landmarks as a background.'
        } // return
      }, // data

     

    }

    console.log(this, "Some log heare");
</script>

<style lang="scss">
  nav {
    background-color: #563d7c;
  }
</style>





















