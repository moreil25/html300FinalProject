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
<!-- nav bar here-->
    <nav class="navbar navbar-expand-lg bg-dark m-3">
      <ul class="list-inline">
        <li class="list-inline-item"><nuxt-link to="/home" class="nav-item text-success">Home</nuxt-link></li>
        <li class="list-inline-item"><nuxt-link to="images" class="nav-item text-danger">Images</nuxt-link></li>
        <li class="list-inline-item"><nuxt-link to="/accordion" class="nav-item text-warning">Professional</nuxt-link></li>
      </ul>
    </nav>

<!--footer here to appear on every page-->

<!--this causes the insersion of router content-->
    <Nuxt />
  </div>
</template>

<style lang="scss">
@import './assets/css/styles.scss';

html {
  font-family: $font-family;
  color: $pink;
  background-color: $blue;
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
