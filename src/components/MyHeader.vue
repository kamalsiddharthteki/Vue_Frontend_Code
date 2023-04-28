<template>
    <div class="header">
        <h1>{{title}}</h1>
        <h3>{{descp}}</h3>
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
    div{
        text-align: center;
        background-color: black;
        color: red;
    }

</style>