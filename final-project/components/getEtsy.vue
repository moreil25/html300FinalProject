<!-- API lists favorited Etsy listings -->
<script>
  export default {
    props: {
      listing: Object
    },
  }
</script>

<template>
 <!-- <div id="get-etsy">
    <b-card title="Listing" sub-title="My Favorites">
      <b-card-text>
        These listings show that the item is still actively available for purchase, as well as the dates they were created</b-card-text>
        <b-card-text>{{ listing.listing_state }}
      </b-card-text>

      <!-- To add the listing created date as a human readable item, would I need to create variables in the script tag or can i just use dot notation in the {{}} since  that indicates a variable in Vue?
      {{ listing.create_date }}
      var d = new Date();
      var n = d.toJSON(); -->

      <a :href="`https://www.etsy.com/listing/${listing.listing_id}`">View Listing</a>
    </b-card>
  </div> -->
