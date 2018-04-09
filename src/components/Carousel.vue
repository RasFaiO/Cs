<template>
  <v-carousel hide-delimiters class="ca1">
    <v-carousel-item v-for="(item,i) in items" :src="item.src" :key="i" transition="fade" reverse-transition="fade"></v-carousel-item>
  </v-carousel>
</template>
<script>
  export default {
    data () {
      return {
        items: [
          { src: 'http://cotrasangil.com/images/banners/banner.jpg' },
          { src: 'http://cotrasangil.com/images/banners/bannertaxis.jpg' },
          { src: 'http://cotrasangil.com/images/banners/bannereds.jpg' },
          { src: 'http://cotrasangil.com/images/banners/BANNERCEPITA.jpg' },
          { src: 'http://cotrasangil.com/images/banners/cdabanner.jpg' }
        ]
      }
    }
  }
</script>
<style lang="stylus">
  .ca1 {
   height: 60%;
  }
</style>