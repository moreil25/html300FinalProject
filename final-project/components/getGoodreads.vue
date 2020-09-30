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
    //where do i use api key?
    mounted() {
      axios
      .get('https://www.goodreads.com/user/compare/1.xml')
      .then(response => (this.books) = response.data)
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
    <h1>Goodreads</h1>
    <div class="single-goodreads">
      <!-- need an element to display data -->
    </div>
  </div>
</template>
