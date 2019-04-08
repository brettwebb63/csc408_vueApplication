<template>
    <div id="app">
      <div id="nav">
          <div class="row">
            <div id ="logosection" class="card" style="background-color: #8AAAE5; border-color: #8AAAE5; align-self: flex-start;">
                <div class="card-body">
                    <img id="myLogo" src="YellowBucketLogoNumberTwo.png">
                </div>
            </div>
            <div id="navbar" class="card">
            <div class="card" style="background-color: #8AAAE5;">
                <div class="card-body">
                    <router-link class="card-text" to="/">Bucket Rentals</router-link>|
                    <router-link class="card-text" to="/customers">Customers</router-link> |
                    <router-link class="card-text" to="/about">About Us</router-link>
                </div>
            </div>
          </div>
      </div>
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
#logosection{
    margin-left: 0rem;
}
    #navbar{
        margin-right: 0rem;
    }
    #myLogo{
        width: 175%;
    }
</style>
