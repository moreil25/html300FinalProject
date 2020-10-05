<script>
import getEtsy from '../components/getEtsy.vue';

export default {
  components: [
    getEtsy
  ],
  data () {
    return {
      //these are the variables that are places in the HTML sections that change based on conditional statements
      header: 'About Me',
      subhead: 'Some Content',
      content: 'I found my way to front-end web development from my enjoyment of fiberarts. Recognizing patterns in cross stitching and crochet led me down this path. My name is Merissa O’Reilly. I come from a blended professional background in community engagement, marketing, and event planning. My educational background began in communications and journalism, where I began as a beat reporter and worked up to a section editor. During that time, I started to gain marketing experience at a small National Historic landmark. As I emerged from these positions, I learned early in my professional beginnings two important things: one, that I would be willing to do what it takes as a team member to create the content we needed (e.g. dress up in historic clothing in the summer in order to create original content for marketing materials), and two, how much I prefer the use of an Oxford comma over the traditional journalistic AP style.  I have shifted focus to continue to grow professionally by diving headfirst into the technology sector. I am currently pursuing a Certificate in Front-End Web Development online at the University of Washington. This program plays to my strengths, continuing to hone my attention to detail; one misplaced punctuation mark and a website can literally grind to a halt. Though it is a challenging pursuit, it is pushing me to grow professionally, inspiring me to rethink how I learn, and showing me beauty in a place that I previously thought was limited to logic.  I would love to bring these experiences to Wirespring and help launch their social media presence and contribute to industry blog content. Digging into research to find nuggets of information that clients are looking to leverage to boost sales and build networks of smart, connected devices with Wirespring’s application enablement platform and cloud services, and deliver messages from a distance with environmentally-friendly, daylight readable displays.',
      notes: 'Etsy API here!'
    }
  }
}
</script>

<template>
  <div>
    <h1 class="display-2 text-center header neon">{{ header }}</h1>
      <div>
        <h2 class="display-3">Why Front-End Web Development?</h2>
        <p class="lead">{{ content }}</p>
      </div>
      <div class="wrapper">
        <h2 class="display-3">Etsy API</h2>
        <!-- v-for="listing in listings" in div, then component getEtsy with v-directives to render a list of items in array
        <getEtsy>
        v-bind="listing.info"
        </geEtsy> -->
      </div>
  </div>
</template>
