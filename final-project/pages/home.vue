<script>
export default {
  data () {
    return {
      //these are the variables that are places in the HTML sections that change based on conditional statements
      header: 'Home',
      showJumbotron: true,
      soon: 'Interact with my site to learn more about my professional achievements and some interesting info about me.',
      // subhead: 'Recently Updated',
      content: 'Experienced community and hospitality management strategist with expertise in community outreach, event coordination, professional writing and editing, and corporate marketing strategies. Works well with a team in an open concept office, individually as a self-starter, and resilient to workplace changes. Professional growth-seeker, strategic thinker, and unabashed user of Oxford commas. I come from a blended professional background in community engagement, marketing, and event planning. My educational background began in communications and journalism, where I began as a beat reporter and worked up to a section editor. During that time, I started to gain marketing experience at a small National Historic landmark. As I emerged from these positions, I learned early in my professional beginnings two important things: one, that I would be willing to do what it takes as a team member to create the content we needed (e.g. dress up in historic clothing in the summer in order to create original content for marketing materials), and two, how much I prefer the use of an Oxford comma over the traditional journalistic AP style.  I have shifted focus to continue to grow professionally by diving headfirst into the technology sector. I am currently pursuing a Certificate in Front-End Web Development online at the University of Washington. This program plays to my strengths, continuing to hone my attention to detail; one misplaced punctuation mark and a website can literally grind to a halt. Though it is a challenging pursuit, it is pushing me to grow professionally, inspiring me to rethink how I learn, and showing me beauty in a place that I previously thought was limited to logic.  I would love to bring these experiences to Wirespring and help launch their social media presence and contribute to industry blog content. Digging into research to find nuggets of information that clients are looking to leverage to boost sales and build networks of smart, connected devices with Wirespring’s application enablement platform and cloud services, and deliver messages from a distance with environmentally-friendly, daylight readable displays.',
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
