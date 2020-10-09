<!-- API lists favorited Etsy listings -->
<script>
  export default {
    props: {
      listing: Object
    },
  }
</script>

<template>

  <div id="get-etsy">
    <b-card title="Listing" sub-title="Favorites">
      <b-card-text>
        These listings show that the item is still actively available for purchase, as well as the dates they were created</b-card-text>
        <b-card-text>{{ listing.listing_state }} {{ listing.create_date }}
      </b-card-text>

      <a :href="`https://www.etsy.com/listing/${listing.listing_id}`">View Listing</a>
    </b-card>
  </div>
  <!-- <div id="get-etsy"> -->
    <!-- v-if loops through favorited listings and displays ones that have active state -->
    <!-- <section class="card" v-if="listing.listing_state == 'active'"> -->
      <!-- <h2 class="card__title">{{ listing.name }}</h2> -->
      <!-- USE AS DEBUGGING TOOL <p>{{ listing }}</p> -->
      <!-- <a :href="`https://www.etsy.com/listing/${listing.listing_id}`">CLICK</a>

      <p class="card__copy">{{ listing.listing_state }} {{ listing.create_date }}</p> -->

      <!--print out a link if it's still active, or date listing was saved -->
    <!-- </section>
    </div> -->
</template>
