<template>
    <div class="header">
        <h1>{{title}}</h1>
        <h2>{{descp}}</h2>
    </div>
    
</template>

<script>
    export default{
        name: 'MyHeader',
        props :{
            title:String,
            descp:String
        }
    }
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Slackey&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Vina+Sans&display=swap');

.header{
    text-align: center;
    background-color: rgb(255, 170, 0); 
    color: rgb(21, 21, 21);
    font-family: 'Slackey', cursive;
}

h1{
    font-size: 45px;
}

h2{
    font-size: 25px;
}

</style>