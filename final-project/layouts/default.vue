<!-- add API and deploy to netlify -->
<!-- add skip to main content link -->
<!-- continue to tweak colors for contrast ratio -->


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
<!-- nav bar here -->
    <nav class="navbar navbar-expand-lg m-3">
      <ul class=" text-center list-inline">
        <li class="list-inline-item"><nuxt-link to="/home" class="nav-item">Home</nuxt-link></li>
        <li class="list-inline-item"><nuxt-link to="/accordion" class="nav-item">Professional</nuxt-link></li>
        <li class="list-inline-item"><nuxt-link to="images" class="nav-item">Images</nuxt-link></li>
        <li class="list-inline-item"><nuxt-link to="/about" class="nav-item">About</nuxt-link></li>
      </ul>
    </nav>
  <div class="header"></div>

<!--footer here to appear on every page, add linked in and github !! NEED TO CHANGED FIXED POSITION-->

<!-- <nav class="navbar fixed-bottom navbar-expand-lg m-3">
  <ul class="list-inline">
    <li class="list-inline-item"><nuxt-link to="/home" class="nav-item">Home</nuxt-link></li>
    <li class="list-inline-item"><a target="_blank" href="https://github.com/moreil25" class="nav-item">GitHub</a></li>
    <li class="list-inline-item"><a target="_blank" href="https://www.linkedin.com/in/merissaoreilly/" class="nav-item">LinkedIn</a></li>
  </ul>
</nav> -->

<!--this causes the insersion of router content-->
    <Nuxt />
  </div>
</template>

<style lang="scss">
@import './assets/css/styles.scss';
@import url('https://fonts.googleapis.com/css2?family=Oswald&family=Sacramento&display=swap');

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
