<template>
    <h3>{{ songs[song] }}</h3>
</template>

<script>
    export default {
        data () {
            return {
                songs: [
                    'Pretty fly for a white guy - The Offspring',
                    'Phoenix - Veil of Maya',
                    'Dave goes to Hollywood - The Black Dahlia Murder',
                    'Angels - Robbie Williams'
                ],
                song: 0
            }
        },
        ready() {
            setInterval(this.nextSong, 2000);
        },
        methods: {
            nextSong(){
                this.song++
                if(this.song >= this.songs.length) {
                    this.song = 0;
                }
            }
        }
    }
</script>