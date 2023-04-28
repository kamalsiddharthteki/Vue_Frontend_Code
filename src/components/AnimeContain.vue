<template>

    <div v-for="anime of animes.animes" :key="anime.id">
        <SingleAnime :anime="anime" />

    </div>
</template>

<script>
import SingleAnime from './SingleAnime.vue'
    export default{
        name : 'AnimeContain',
        props : {
            animes : Array
        },
        components:{
            SingleAnime
        }
    }
</script>

<style scoped>

</style>