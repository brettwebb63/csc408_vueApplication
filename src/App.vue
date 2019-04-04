<template>
    <div id="app">
      <div id="nav">
        <router-link class="logo" to="/Movies">Bucket Rentals</router-link> |
        <router-link to="/customers">Customers</router-link> |
        <router-link to="/about">About Us</router-link>
      </div>
      <router-view/>
    </div>
</template>

<style lang="scss">
/* Add Google Font */
@import url('https://fonts.googleapis.com/css?family=Open+Sans:300,400,700');

/* This is where we import our custom CSS files */
@import './assets/styles/custom.css';

#app {
  font-family: 'Open Sans', Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #ffffff;
    &.router-link-exact-active {
      color: #65580D;
    }
  }
    .logo{
        text-align: left;
    }
}
</style>
