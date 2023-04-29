<template>
    <div class="animecontainer">
        <h1 class="name">{{ anime.name }}</h1>
        <img :src="anime.image">
        <h2>Studio : {{ anime.studios }}</h2>
        <h3> Aired on : {{ anime.airedon }}</h3>
        <h3>Episodes : {{ anime.episodes }}</h3>
        <h3>Rating : {{ anime.rating }}</h3>
        <h3 class="description">Description : {{ anime.description }}</h3>
    </div>
    
</template>

<script>
    export default{
        name : 'SingleAnime',
        props : {
            anime : Array
        }
    }
</script>

<style scoped>
.animecontainer{
    background-color: rgb(255, 170, 0);
    text-align: center;
    color: white;
    border-radius: 60px;
}

img{
    width: 220px;
    height: 300px;
    box-shadow: 5px 5px 20px black;
}

.description{
    text-align: justify;
    padding : 5%;
}

.name{
    padding-top: 5%;
}

</style>