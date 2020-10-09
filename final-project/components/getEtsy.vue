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
