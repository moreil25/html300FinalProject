<script>
export default {
  data () {
    return {
  //these are the variables that are places in the HTML sections that change based on conditional statements
      header: 'Professional',
      subheads: [
        {
          name: 'Professional Background'
        },
        {
          name: 'Volunteer Experience'
        },
      ],

      contents: [
        {
          id: 1,
          title: 'Marketing',
          quote: 'Managed a corporate Facebook account, updating content bi-weekly, to see monthly engagement rates increase one to two percent over a six month period. Contributed blog content. Utilized Mailchimp and Square to develop marketing materials and deploy an online retail store.',
          tip: 'Professional experience'
        },
        {
        id: 2,
        title: 'Executive Events',
        quote: 'Led all planning and execution of logistics for inaugural Sustainable Hospitality Developmentt Symposium from beginning to end in eight months. Managed volunteers for all community outreach events. Coordinated all aspects of Masters Week® hospitality house, with daily rotating guest list, in-house catering, restaurant reservations, transportation to and from all events, and personalized welcome gifts.',
        tip: 'Professional experience'
        },
        {
        id: 3,
        title: 'Executive Admin',
        quote: 'Navigated all levels of contracting services witth vendors internally and externally. Maintained well-organized system for confidential files and financial records, ensuring 100% compliance with standardized requirements and federal policies.',
        tip: 'Professional experience'
        },
        {
        id: 4,
        title: 'SFRG Treasurer',
        quote: 'Over the last year and a half, I have given my time to my local Soldier and Family Readiness Group (SFRG) in various ways, mainly as the treasurer for my local chapter. I was the main organizer of several events that required marketing to a small, specific target audience to maximize attendance. In addition to raising attendance at these events from 30 people to 45 or more people, I worked with soldiers to create specific events geared toward them. Drawing on my past profesisonal experience, I mapped and developed a 45 minute walking tour of downtown Augusta, GA, that highlighted local art, local businesses, and historic locations. The primary goal of developing this resource was to help bring fellowship and a sense of belonging to military spouses. I manage an inventory of merchandise used to raise funds for annual reunion events, and have used Weebly to launch an eCommerce store to accomodate a larger audience.',
        tip: 'Volunteer experience'
        },
        {
        id: 5,
        title: 'R.I.S.E. Representative',
        quote: 'I have recently accepted a position as a committee member for R.I.S.E. of the Legion, a group that supports relationship information support and empowerment (R.I.S.E.). We plan events throughout the year that help military spouses connect with each other to work toward building positive relationships with their peers by building mutual support. Most of these events feature an educational aspect with guest speakers, nutritional information, conflict management, and more.',
        tip: 'Volunteer experience'
        },
        {
        id: 6,
        title: 'Augusta Handmade Fair Representative',
        quote: 'I served as a steering committee member for the Augusta Handmade Fair for a year. The A.H.F. is a twice-a-year juried event that is focused on showcasing regional creatives in an array of mediums such as: art, home decor, apparel & accessories, pottery, bath & body, gifts, and more, while supporting a larger mission to assist a sister organziation in Uganda. As a committee member, I assisted in selecting the artisans, planning additional activities for the community members who attended, worked with sponsors,  and managed live social media during the Augusta Handmade Fair.',
        tip: 'Volunteer experience'
      },
      ],
    }
  },
  head() {
      return {
        title: this.header,
        meta: [
          {
            hid: 'professional',
            name: 'experience',
            content: 'experience in professional positions'
          }
        ]
      }
    }
  }

</script>

<template>
  <div>
    <h1 class="display-1 text-center header neon">{{ header }}</h1>
  <div>
    <a href="#main-content" class="hidden">Skip to main content!!</a>
    <h2>{{ subhead }}</h2>
    <p class="lead">I come from a blended professional background in community engagement, marketing, and event planning. My educational background began in communications and journalism, where I began as a beat reporter and worked up to a section editor. During that time, I started to gain marketing experience at a small National Historic landmark. As I emerged from these positions, I learned early in my professional beginnings two important things: one, that I would be willing to do what it takes as a team member to create the content we needed (e.g. dress up in historic clothing in the summer in order to create original content for marketing materials), and two, how much I prefer the use of an Oxford comma over the traditional journalistic AP style.  I have shifted focus to continue to grow professionally by diving headfirst into the technology sector. I am currently pursuing a Certificate in Front-End Web Development online at the University of Washington. This program plays to my strengths, continuing to hone my attention to detail; one misplaced punctuation mark and a website can literally grind to a halt. Though it is a challenging pursuit, it is pushing me to grow professionally, inspiring me to rethink how I learn, and showing me beauty in a place that I previously thought was limited to logic.  </p>

<!--manual accordion to get it working THEN do iteration through blurbs-->
<!--use aria-expanded to convey state of collapsable elements to screen readers and other assistive technology-->
<!--each card groups together similar information-->

  <div class="accordion text-center" id="accordion">
    <h2 v-for="subhead in subheaders" v-bind="subhead.name"></h2>
<!--v-for content on contets dynamic cards that will loop through data in array-->
<!--used bootstrap-vue elements-->
<!--key element is used to "hint" to the DOM to identify vnodes-->
<!--use dot notation to access data, including id to generate a unique id for each item to be toggled-->
  <b-card v-for="content in contents" v-bind:key="content.id" >
    <b-card-header id="headingOne">
      <h3 v-b-tooltip.hover :title="content.tip"><b-button type="button" size="lg" pill variant="outline-secondary" v-b-toggle="'content-' + content.id" aria-expanded="false" aria-controls="collapseOne">{{ content.title }}</b-button>
      </h3>
    </b-card-header>
    <b-collapse :id="'content-' + content.id" accordion="accordionOne" aria-labelledby="headingOne">
      <b-card-body>{{ content.quote }}</b-card-body>
    </b-collapse>
  </b-card>
  </div>
</div>
</div>

</template>
