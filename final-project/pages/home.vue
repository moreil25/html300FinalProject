<script>
export default {
  data () {
    return {
      //these are the variables that are places in the HTML sections that change based on conditional statements
      header: 'Home',
      showJumbotron: true,
      soon: 'Interact with my site to learn more about my professional achievements and some interesting info about me.',
      // subhead: 'Recently Updated',
      content: 'Experienced community and hospitality management strategist with expertise in community outreach, event coordination, professional writing and editing, and corporate marketing strategies. Works well with a team in an open concept office, individually as a self-starter, and resilient to workplace changes. Professional growth-seeker, strategic thinker, and unabashed user of Oxford commas.',
      notes: 'My short term professional goal is to become a better a11y (ally) in implementing web accessibility. There are very easy things that businesses can do to open digital accessibility to more of their audience, and these changes aren’t solely reliant on the web development segment of their teams. As web development professionals, we can collaborate with our clients to begin to design products to better suit these needs, and in very simple ways, such as making sure color palettes include contrast ratios that maximize readability. I also plan to become more proficient in ES6+ syntax.'
    }
  }
}
</script>

<template>
  <div>
    <h1 class="display-1 text-center header neon">{{ header }}</h1>
      <div class="jumbotron" v-if="showJumbotron">
        <h2 class="display-3 text-center header-two">Welcome!</h2>
        <p class="font-weight-bold text-center">{{ soon }}</p>
        <!-- v-on:click enables button to change content if clicked, otherwise content is shown due to != making it false-->
        <button v-on:click="showJumbotron = !showJumbotron">Show</button>
      </div>
      <div class="jumbotron" v-else="showJumbotron">
        <h2 class="display-3 text-center header-two-alt">Updates Coming Soon</h2>
        <p class="font-weight-bold text-center">{{ soon }}</p>
        <!-- v-on:click enables button to change content if clicked, otherwise content is shown due to != making it false-->
        <button v-on:click="showJumbotron = !showJumbotron">Show</button>
      </div>
      <div>
        <h2 class="display-4">Merissa O'Reilly</h2>
        <p class="lead">{{ content }}</p>
      </div>
      <div>
        <h2 class="display-4">Short Term Goal</h2>
        <p class="lead">{{ notes }}</p>
      </div>
  </div>
</template>
