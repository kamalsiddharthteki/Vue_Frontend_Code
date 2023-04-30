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
        const res=await fetch("https://nodejs-backend-ts3u.onrender.com/api")
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
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,600&display=swap');

#container{
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  gap: 100px;
  justify-content: space-evenly;
}

#app{
  background-color: rgb(21, 21, 21);
}

html{
  background-color: rgb(21, 21, 21);
}
</style>