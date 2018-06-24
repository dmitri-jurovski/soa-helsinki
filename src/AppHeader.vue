<template>

    <b-navbar sticky toggleable="true" type="light" variant="purple" style="background-color: #563d7c;">
    <b-container>
    <b-navbar-brand href="#">soa.Helsinki</b-navbar-brand>
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

  

  <b-collapse is-nav id="nav_collapse">

    <b-navbar-nav>
      <b-nav-item href="#">Link</b-nav-item>
      <b-nav-item href="#" disabled>Disabled</b-nav-item>
    </b-navbar-nav>

    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto">

    
Book your personal photo shoot, to keep your memories of your day with a private photo shoot using Helsinki major landmarks as a background.
   

    
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
</script>

<style>
  nav {
    background-color: #563d7c;
  }
</style>





















