<!-- API lists favorite Etsy shops BUT I need to find out what data is available to use -->
<script>
  export default {
    props: {
      listing: Object
    },
  }
//     where do i use api key? in the url  6kutd3kmmvov61bbwo41jzx3  /users/Merissa/favorites/listings


</script>

<template>
  <div id="get-etsy">
    <h1>Etsy</h1>
    <section class="card" v-if="listing.listing_state == 'active'">
      <!-- USE AS DEBUGGING TOOL <p>{{ listing }}</p> -->
      <a :href="`https://www.etsy.com/listing/${listing.listing_id}`">CLICK</a>
      <h2 class="card__title">{{ listing.name }}</h2>
      <p class="card__copy">{{ listing.listing_state }}</p>
      <!--print out a link if it's still active, or date listing was saved -->
    </section>
    </div>
</template>
