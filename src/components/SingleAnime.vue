<template>
    <div class="container">
        <div class="animecontainer">
            <h1 class="name">{{ anime.name }}</h1>
            <img :src="anime.image">
            <h2>Studio : {{ anime.studios }}</h2>
            <h2> Aired on : {{ anime.airedon }}</h2>
            <h2>Episodes : {{ anime.episodes }}</h2>
            <h2>Rating : {{ anime.rating }}</h2>
        </div>
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
@import url('https://fonts.googleapis.com/css2?family=Vina+Sans&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Balsamiq+Sans&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Bangers&display=swap');
.animecontainer{
    background-color: rgb(255, 140, 0);
    text-align: center;
    border-radius: 20px;
}

.animecontainer:hover{
    background-color: rgb(255, 98, 0);
}

img{
    width: 60%;
    height: 300px;
    min-height: 200px;
    box-shadow: 5px 5px 20px black;
}

.description{
    text-align: justify;
    padding : 5%;
    color: rgb(255, 170, 0);
}

.name{
    padding-top: 5%;
    font-size: 40px;
}

h1, h2, h3{
    /* text-shadow: 1px 1px 4px black; */
    font-family: 'Vina Sans', cursive;
    color:rgb(21, 21, 21);
}

h3{
    font-family: 'Balsamiq Sans', cursive;
}

h1{
    font-family: 'Bangers', cursive;
}

</style>