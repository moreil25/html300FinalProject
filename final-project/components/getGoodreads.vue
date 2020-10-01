<!-- API compares books with another goodreads member -->
<script>
const axios = require('axios');
  export default {
    data() {
      return {
        loading: true,
        books: null,
        errored: false
      }
    },
    //where do i use api key?   6kutd3kmmvov61bbwo41jzx3  /users/Merissa/favorites/listings
    mounted() {
      axios
      .get('https://openapi.etsy.com/v2/users/Merissa/favorites/listings.js?api_key=6kutd3kmmvov61bbwo41jzx3')
      .then(response => console.log(response))
      .catch(error => {
        console.log(error)
        this.errored = true
      })
      .finally(() => this.loading = false)
    }
  }
</script>

<template>
  <div id="get-goodreads">
    <h1>Etsy</h1>
    <div class="single-goodreads">
      <!-- need an element to display data, look through data keys and select a few of the listings -->
    </div>
  </div>
</template>
