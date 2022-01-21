<template>
  <header>

    <nav class="container">
      <router-link v-on:click="closeMenu" to="/">
        <img
          id="logo"
         src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg"
         alt="WDEV"
         >
      </router-link>

      <img
       v-on:click="openMenu"
       id="menu-button"
       src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg"
       alt="abrir menu"
       >

       <div id="menu-overlay" v-on:click="closeMenu" v-if="menuIsActive" />

       <div id="menu-items" :class="{active:menuIsActive}">
        <img
          id="menu-logo"
         src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg"
         alt="WDEV"
         >

        <ul>
          <li v-on:click="closeMenu"><router-link to="/">Home</router-link></li>
          <li v-on:click="closeMenu"><router-link to="/videos">Video</router-link></li>
          <li v-on:click="closeMenu"><router-link to="/sobre">Sobre</router-link></li>
          <li v-on:click="closeMenu"><router-link to="/contato">Contato</router-link></li>
        </ul>
       </div>


    </nav>

  </header>
</template>

<script>

  export default {
    name: 'Header',

    data() {
      return {
        menuIsActive: false
      }
    },

    methods: {

    openMenu() {
      this.menuIsActive = true;
    },

    closeMenu() {
      this.menuIsActive = false;
    }

    }

  }

</script>

<style scoped>

    header {
      background-color: var(--color-background-nav);
      height: 60px;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
  }

    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 60px;
    }

    #logo {
      width: 130px;
  }

  #menu-button {
      width: 30px;
      cursor: pointer;
  }

  #menu-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: black;
    opacity: 0.8;
  }

  #menu-items {
    position: fixed;
    top: 0;
    right: -100%;
    width: 60%;
    height: 100vh;
    background-color: var(--color-background-nav) ;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    transition: 0.5s right;
  }

  #menu-logo {
    width: 110px;
    margin-top: 30px;
    margin-bottom: 10px;
  }

  ul li {
    text-align: center;
    margin: 20px 0;
  }

  ul li a {
    color: var(--color-text-light);
  }

  #menu-items.active {
    right: 0px;
  }

  /** Desktop */
  @media (min-width: 700px) {
    #menu-button,
    #menu-logo,
    #menu-overlay {
      display: none;
    }

    #menu-items {
      display: flex;
      position: static;
      height: 60px;
      width: auto;
    }

    ul {
      display: flex;
      align-items: center;
      height: 60px;
    }

    ul li {
      margin: 0;
      margin-left: 20px;
    }
  }

  

</style>