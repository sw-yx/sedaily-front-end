<template>
  <div id='sticky-player'>

        <a-player :music="{
          title: this.$store.state.activePlayerItem.title.rendered || ' ',
          author: ' ',
          url: this.$store.state.activePlayerItem.mp3 || ' ' ,
          pic: this.$store.state.activePlayerItem.featuredImage || ' ',
          lrc: '[00:00.00]lrc here\n[00:01.00]aplayer'
        }"></a-player>

  </div>
</template>

<script>
/* @flow */
import VueAplayer from './VuePlayerClone.vue'

export default {
  name: 'sticky-player',
  components: {
    'a-player': VueAplayer
  },
  data () {
    return {
      playingItem: null
    }
  }
}
</script>

<style scoped>
  #bigDiv{
    height:150vh
  }

  #toolbar{
    position:sticky;
    top:1px;
  }
</style>
