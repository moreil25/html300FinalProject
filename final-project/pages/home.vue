<script>
export default {
  data () {
    return {
      //these are the variables that are places in the HTML sections that change based on conditional statements
      header: 'Home',
      showJumbotron: true,
      soon: 'Jumbotron Coming Soon!',
      subhead: 'Some Content',
      content: 'Add some content here, then add the card section from Lesson 03 as component',
      notes: 'Add API here!'
    }
  }
}
</script>

<template>
  <div>
    <h1 class="display-1 text-center">{{ header }}</h1>
      <div class="jumbotron" v-if="showJumbotron">
        <h2 class="display-3 text-center bg-secondary">Content</h2>
        <p class="font-weight-bold">{{ soon }}</p>
        <!-- v-on:click enables button to change content if clicked, otherwise content is shown due to != making it false-->
        <button v-on:click="showJumbotron = !showJumbotron">Show</button>
      </div>
      <div class="jumbotron" v-else="showJumbotron">
        <h2 class="display-3 text-center bg-danger">Different Content</h2>
        <p class="font-weight-bold">{{ soon }}</p>
        <!-- v-on:click enables button to change content if clicked, otherwise content is shown due to != making it false-->
        <button v-on:click="showJumbotron = !showJumbotron">Show</button>
      </div>
      <div>
        <h2 class="display-">{{ subhead }}</h2>
        <p class="lead">{{ content }}</p>
      </div>
      <div>
        <h2 class="display-2">{{ subhead }}</h2>
        <p class="lead">{{ notes }}</p>
      </div>
  </div>
</template>
