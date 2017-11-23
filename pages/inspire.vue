<template>
  <v-container fluid>
    <v-layout>
      <v-carousel>
        <v-carousel-item v-for="(item,i) in items" v-bind:src="item.src" :key="i"></v-carousel-item>
      </v-carousel>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: '/slide1.jpg'
          },
          {
            src: '/slide2.jpg'
          },
          {
            src: '/slide3.jpg'
          }
        ]
      }
    }
  }
</script>
