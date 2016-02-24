<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <player></player>
    <show></show>
    <song></song>
  </div>
</template>

<script>
import Player from './components/Player.vue'
import Show from './components/Show.vue'
import Song from './components/Song.vue'

export default {
  components :{
    Player,
    Show,
    Song
  },
  data () {
    return {
      msg: 'Awesome Radio Show!'
    }
  }
}
</script>

<style>
body {
  font-family: Helvetica, sans-serif;
}
</style>
