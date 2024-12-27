<script setup>
import {trainers} from '../assets/data/data.js'
</script>
<template>
    <section class="trainers_container" id="trainers">
        <h2>TOP TRAINERS</h2>
        <div class="trainers">
            <picture v-for="data in trainers" :key="data.id">
                <img :src="data.photograph" alt="">
                <h6>{{data.name}}</h6>
            </picture>
        </div>
        <h3>Professionals ready to make <br/>your 
            journey <span class="orange">healthy and easier</span></h3>
    </section>
</template>
<style scoped>
.trainers_container{
    background-color:#000;
    margin: auto;
    color:#fff;
}

.trainers{
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    gap:60px;
    margin:40px 0px;
   
}
h2,h3{
    margin: auto;
    max-width: 1200px;
    padding: 20px;
    font-size:40px;
    padding-top:60px;
}
h6{
    margin:0;
    font-size:20px;
}
h3{
    text-align:end; 
    margin-top:100px;
}
picture{
    width:200px;
    height: 200px;
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:20px;
    img{
        width:100%;
    }
}

@media(min-width:768px){
    .trainers{
        flex-direction:row;
        justify-content:space-around;
    }
}

</style>