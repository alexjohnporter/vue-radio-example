<template>
    <h2>{{ shows[show] }}</h2>
</template>

<script>
    export default {
        data () {
            return {
                shows: [
                    'Morning',
                    'Lunch',
                    'Dinner',
                    'Evening'
                ],
                show: 0
            }
        },
        ready() {
            setInterval(this.nextShow, 3000);
        },
        methods: {

            nextShow(){
                this.show++
                if(this.show >= this.shows.length) {
                    this.show = 0;
                }
            }
        }
    }
</script>
