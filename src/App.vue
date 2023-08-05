<template>
  <div id="wrapper">
    <nav class="navbar is-link">
      <div class="navbar-brand">
        <!-- SIDE LEFT -->
        <router-link to="/" class="navbar-item"><strong>TusMotos.com</strong></router-link>

        <a href="" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbar-menu" @click="showMobileMenu = !showMobileMenu">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <!-- SIDE RIGHT -->
      <div class="navbar-menu" id="navbar-menu" v-bind:class="{'is-active': showMobileMenu}">
        <div class="navbar-end">
          <router-link to="/scooters" class="navbar-item">Scooters</router-link>
          <router-link to="/electricas" class="navbar-item">Eléctricas</router-link>
          <div class="navbar-item">
            <div class="buttons">
              <router-link to="/log-in" class="button is-light">Log In</router-link>
              <router-link to="/cart" class="button is-success">
                <span class="icon"><i class="fas fa-shopping-cart"></i></span>
                <span>Cart</span>
              </router-link>
            </div>
          </div>
        </div>
      </div>
    </nav> 

    <section class="section">
      <router-view/>
    </section>
    <footer class="footer">
      <p class="has-text-centered">Copyright (c) 2023</p>
    </footer>
  </div>
</template>

<script>
  export default{
    data(){
      return {
        showMobileMenu: false,
      }
    }
  }
</script>

<style lang="scss">
  @import '../node_modules/bulma';
</style>
