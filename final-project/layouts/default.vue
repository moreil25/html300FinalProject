<!-- add API and deploy to netlify -->
<!-- add skip to main content link -->
<!-- continue to tweak colors for contrast ratio -->
<!-- use a popover somewhere? -->



<script>
export default {
  name: 'App',
  data () {
    return {
      msg: 'Hello'
    }
  }
}
</script>

<template>
  <div id="app">
<!-- nav bar using Bootstrap Vue to include a dropdown section -->
    <div class="menu">
      <b-navbar toggleable="lg" type="dark">
        <b-navbar-nav>
          <b-nav-item><nuxt-link to="/home">Home</nuxt-link></b-nav-item>
          <b-nav-item-dropdown text="About" right>
            <b-dropdown-item><nuxt-link to="/accordion">Professional</nuxt-link></b-dropdown-item>
            <b-dropdown-item><nuxt-link to="/about">About</nuxt-link></b-dropdown-item>
          </b-nav-item-dropdown>
          <b-nav-item><nuxt-link to="/images">Images</nuxt-link></b-nav-item>
        </b-navbar-nav>
      </b-navbar>
    </div>
  <div class="header"></div>



<!--this causes the insersion of router content-->
    <Nuxt />
    <!--footer here to appear on every page, NEED TO CHANGE FIXED POSITION to make sticky footer???-->
    <div class="footer">
      <b-navbar toggleable="lg" type="dark">
        <b-navbar-nav>
          <b-nav-item target="_blank" href="https://github.com/moreil25" class="nav-item">GitHub</b-nav-item>
          <b-nav-item target="_blank" href="https://www.linkedin.com/in/merissaoreilly/" class="nav-item">LinkedIn</b-nav-item>
        </b-navbar-nav>
      </b-navbar>
    </div>
  </div>
</template>

<style lang="scss">
@import './assets/css/styles.scss';
@import url('https://fonts.googleapis.com/css2?family=Oswald&family=Sacramento&display=swap');
/*main body content needs to have bottom margin same height as footer, set footer height manually in CSS*/

html {
  font-family: $font-family;
}
p {
  color: $turquoise;
}
h1, h2, h3 {
  color: $rust;
}
/*add background url? */
.header{
  font-family: $font-family-alt;
  background-image: url('../assets/ceiling.jpg');
}
.header-two {
  background-color: $teal;
}
.header-two-alt {
  background-color: $turquoise;
}
body {
  background-color: $cream;
}
.jumbotron {
  background-color: $brick;
}
.accordion {
  border: solid 2px gray;
}
a {
  color: $cream;
}
a:hover {
  text-decoration: none;
  color: $teal;
}
nav {
  background-color: $rust;
}
.neon {
  color: #ffffff;
  text-shadow:
    0 0 5px #ffffff,
    0 0 10px #ffffff,
    0 0 20px #ffffff,
    0 0 40px $turquoise,
    0 0 80px $turquoise,
    0 0 90px $turquoise,
    0 0 100px $turquoise,
    0 0 150px $turquoise;
}


*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}
.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}
.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}
.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

</style>
