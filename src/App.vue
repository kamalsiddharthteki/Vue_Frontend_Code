<template>
  <div id="header">
    <MyHeader title="Top 6 Anime" descp="Anime recommendation by Kamal Siddharth Teki"/>
  </div>
  <div id="container">
    <AnimeContain :animes=animes /> 
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import AnimeContain from './components/AnimeContain.vue'
  export default{
    name: 'App',
    components: {
      MyHeader,
      AnimeContain
    },
    data(){
      return{
        animes: []
      }
    },
    methods:{
      async fetchAnime(){
        const res=await fetch("https://nodejs-backend-ts3u.onrender.com")
        const data=await res.json()
            console.log(data)
        return data
      }
    },
    async created(){
      this.animes = await this.fetchAnime()
    }
  }
</script>

<style>
#container{
  background-color: black;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  grid-column-gap: 5%;
  margin: 0 5%;
}

#app{
  background-color: black;
}

html{
  background-color: black;
}


</style>