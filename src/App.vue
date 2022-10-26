<template>
  <div id="app">

    <b-navbar toggleable="lg" type="dark" variant="dark" v-if="notIsLoginPage">
    
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">Modalidades</b-nav-item>
          <b-nav-item href="#" >Notícias</b-nav-item>
          <b-nav-item href="#" >Minha conta</b-nav-item>
        </b-navbar-nav>
    
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
    
          <b-nav-item right>
            Log Out
          </b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

    <router-view/>
  </div>
</template>

<script>
  export default{
    computed:{
      notIsLoginPage(){
        return this.$route.name !== "login";
      }
    }
  }

</script>

<style>

</style>
