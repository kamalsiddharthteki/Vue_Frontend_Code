<template>
    <div v-for="anime of animes.animes" :key="anime.id" class="card-container">
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
.card-container{
    width:300px;
}
</style>