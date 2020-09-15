<template>
  <div>
    <h1 class="display-1">{{ header }}</h1>

  <div>
    <h2>{{ subhead }}</h2>

<!--manual accordion to get it working THEN do iteration through blurbs-->
<!--use aria-expanded to convey state of collapsable elements to screen readers and other assistive technology-->
<!--each card groups together similar information-->

  <div class="accordion" id="accordion">
<!--v-for content on contets dynamic cards that will loop through data in array-->
<!--used bootstrap-vue elements-->
<!--key element is used to "hint" to the DOM to identify vnodes-->
<!--use dot notation to access data, including id to generate a unique id for each item to be toggled-->
  <b-card v-for="content in contents" v-bind:key="content.id" >
    <b-card-header id="headingTwo">
      <h3><b-button type="button" v-b-toggle="'content-' + content.id" aria-expanded="false" aria-controls="collapseTwo">{{ content.title }}</b-button>
      </h3>
    </b-card-header>
    <b-collapse :id="'content-' + content.id" accordion="accordionOne" aria-labelledby="headingTwo">
      <b-card-body>{{ content.quote }}</b-card-body>
    </b-collapse>
  </b-card>
  </div>
</div>
</div>
</template>



<script>
export default {
  data () {
    return {
  //these are the variables that are places in the HTML sections that change based on conditional statements
      header: 'About Me',
      subhead: 'Professional Background',
      contents: [
        {
          id: 1,
          title: 'Marketing Experience',
          quote: 'Managed a corporate Facebook account, updating content bi-weekly, to see monthly engagement rates increase one to two percent over a six month period. Contributed blog content. Utilized Mailchimp and Square to develop marketing materials and deploy an online retail store.'
        },
        {
        id: 2,
        title: 'Executive Event Experience',
        quote: 'Led all planning and execution of logistics for inaugural Sustainable Hospitality Developmentt Symposium from beginning to end in eight months. Managed volunteers for all community outreach events. Coordinated all aspects of Masters Week® hospitality house, with daily rotating guest list, in-house catering, restaurant reservations, transportation to and from all events, and personalized welcome gifts.'
        },
        {
        id: 3,
        title: 'Executive Admin Experience',
        quote: 'Navigated all levels of contracting services witth vendors internally and externally. Maintained well-organized system for confidential files and financial records, ensuring 100% compliance with standardized requirements and federal policies.'
        },

      ],
  }

    }
  }

</script>
