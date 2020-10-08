<!-- API lists favorite Etsy shops BUT I need to find out what data is available to use -->
<script>
  export default {
    props: {
      listing: Object
    },
    data() {
    },
  }
//     where do i use api key? in the url  6kutd3kmmvov61bbwo41jzx3  /users/Merissa/favorites/listings
// .get, .then, .catch, and .finally are methods chained together to handle results and errors
// should this part be in index.vue?

</script>

<template>
  <div id="get-etsy">
    <h1>Etsy</h1>
    <section class="card" v-if="listings">
      <!-- <getEtsy
        v-for="listing of listings"
        :key="listing.id"
        :listing="listing"
        /> -->
    <!-- how do you know what values in the data are images, etc? i.e. I would expect the listing_id to be an image but how do you know for sure? -->
      <!--<img :src="this.listing_id" :alt="this.alt" class="card__img">
      <h2 class="card__title">{{ listing.name }}</h2>
      <p class="card__copy">{{ listing.content }}</p>-->
    </section>
    </div>
</template>
