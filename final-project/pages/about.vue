<script>
import axios from 'axios';
import getEtsy from '../components/getEtsy.vue';

export default {
  components: {
    getEtsy
  },
  data () {
    return {
      //these are the variables that are places in the HTML sections that change based on conditional statements
      header: 'About Me',
      subhead: 'Some Content',
      content: 'I found my way to front-end web development from my enjoyment of fiberarts. Recognizing patterns in cross stitching and crochet led me down this path.',
      notes: 'Etsy API here!',

    loading: true,
    listings: null,
    errored: false
  }
  },
//API key 6kutd3kmmvov61bbwo41jzx3
  //.get, .then, .catch, and .finally are methods chained together to handle results and errors
  mounted() {
  //This is a good debugging tool to confirm the function is running as expected
  //console.log('mounted function started');
  axios
  .get('https://openapi.etsy.com/v2/users/r6g3usxn/favorites/listings.json?api_key=6kutd3kmmvov61bbwo41jzx3')
  .then((response) => {
    //For some reason, Etsy API does not require you to tell it to use JSON
    //const data = JSON.parse(response.data)
    console.log(response.data.results); this.listings = response.data.results}
  )
  .catch(error => {
    console.log(error)
    this.errored = true
  })
  .finally(() => {console.log('done'); this.loading = false})
  }
  }
</script>

<template>
  <div>
    <h1 class="display-1 text-center header neon">{{ header }}</h1>
      <div>
        <h2 class="display-3">Why Front-End Web Development?</h2>
        <p class="lead">{{ content }}</p>
      </div>
      <div class="wrapper">
        <h2 class="display-3">These Are a Few of My Favorite Things</h2>
        <!-- v-if lets us know that if the listings array is returned null, we do not want to dislpay  anything -->
      <div v-if="listings !== null">
        <!-- v-for="listing in listings" in div, then component getEtsy with v-directives to render a list of items in array -->
    <getEtsy
            v-for="listing in listings"
            :key="listing.listing_id"
            :listing="listing"
              />
      </div>
  </div>
</div>
</template>
