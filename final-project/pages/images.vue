<!--would like to revisit this project and implement carousel-->

<script>
import clickableImage from '../components/clickableImage.vue';

export default {
  components: {
    clickableImage
  },
  data () {
    return {
  //these are the variables that are placed in the HTML sections that change based on conditional statements
      header: 'Images',
        images: [
          {
          img: 'Cross Stitch',
          src: 'xstitch2.jpg',
          caption: 'Cross Stitch Flat Lay',
          alt: 'Flat lay image of several cross stitch pieces'
        },
        {
          img: 'Lions',
          src: 'lions.jpg',
          caption: 'Crocheted Lions',
          alt: 'Two small crocheted lions'
        },
        {
          img: 'Rainbow',
          src: 'rainbow.jpg',
          caption: 'Crocheted Rainbow',
          alt: 'Crocheted rainbow'
        },
        {
          img: 'Close Up Knit',
          src: 'knit.jpg',
          caption: 'Moss Stitch Close Up',
          alt: 'Close up view of changing yarn colors in knit'
        },
        {
          img: 'Start of Knitting',
          src: 'knit-start.jpg',
          caption: 'Cast On with New Yarn',
          alt: 'Knitting needle with cast on yarn, balls of yarn'
        }
      ]
    }
  },
  head() {
      return {
        title: this.header,
        meta: [
          {
            hid: 'images',
            name: 'images',
            content: 'custom images curated by me'
          }
        ]
      }
    }
}

</script>

<!-- alt text appears as tool tip on each image using v-b-tooltip directive-->
<template>
  <div>
    <h1 class="display-1 text-center header neon">{{ header }}</h1>
      <div class="col-lg-12 wrapper">
        <a href="#main-content" class="hidden">Skip to main content!!</a>
<!-- v-for will have to go in a wrapper for each image (i.e. div) and create props for components-->
    <!--v-for directive renders a list of items in array, imageOne in images loops through that array//:src function refers to method created to pull images from source directory//dot notation calls on key values in object-->
    <div class="wrapper" v-for="imageOne in images">
      <clickableImage
        v-bind:img="imageOne.img"
        v-bind:src="imageOne.src"
        v-bind:caption="imageOne.caption"
        v-bind:alt="imageOne.alt"
        v-b-tooltip.hover :title="imageOne.alt">
      </clickableImage>
    </div>
    </div>
  </div>
</template>
