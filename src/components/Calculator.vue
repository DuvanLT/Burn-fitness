<script setup lang="ts">
import { ref } from 'vue'
const imc = ref<number>(0)
const weight = ref<number | null>(null)
const height = ref<number | null>(null)
const status = ref<string>('')
    const imc_calculator = () => {
        if (weight.value !== null && height.value !== null) {
        imc.value = weight.value / ((height.value / 100) * (height.value / 100))
        if(imc.value < 18.5){
            status.value = 'Underweight'
        }else if(imc.value >= 18.5 && imc.value < 24.9){
            status.value = 'Normal weight'
        }else if(imc.value >= 25 && imc.value < 29.9){
            status.value = 'Overweight'
        }
    }
}
</script>
<template> 
<h2 id="calculator">IMC CALCULATOR</h2>
<div class="calculator_container">
<!--@submit... allows to prevent the load of the page and bind the form with a function-->
<form @submit.prevent="imc_calculator">
    <p>The IMC CALCULATOR help to you to know your current relationship between your weight and your height   </p>
    <label><b class="orange">Height</b><b> (cm)</b></label>
    <input type="number"  v-model="height" id="height" placeholder="174" >
    <label><b class="orange">Weight</b> <b>(kg)</b></label>
    <input type="number"  v-model="weight" id="weight" placeholder="70">
    <button type="submit">CALCULATE</button>
    <p v-if="imc > 0">{{imc.toFixed(1)}} {{status}}</p>
</form>
<picture>
    <img src="../../public/multimedia/calculator_women.jpg" alt="">
</picture>
</div>
</template>
<style scoped>
h2{
    text-align: center;
    font-size: 30px;
    color: #cf6500;
    margin-top: 60px;
}

button{
    color: #cf6500;
}

button:hover{
    color: #fff;
}

.calculator_container{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 40px;
    padding: 20px;
    background-color: #f5f5f5;
    max-width: 1200px;
    margin: 60px auto;

    p{
        font-weight: 600;
    }
}
input{
    padding: 8px 14px;
    background: #d9d9d9;
    border: none;
}
form{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
}
picture{
    width:300px;
    height:350px;
    display:flex;
    align-items:center;
    img{
        width:100%;
        height: 100%;
        object-fit: cover;
    }
}

@media (min-width: 768px) {
    .calculator_container{
        flex-direction: row;
        padding: 20px;
        justify-content: space-between;

        p{
            font-size: 20px;
        }
    }


    picture{
        width: 600px;
        height: 500px;
    }

    label, input{
        font-size: 20px;
    }

    form{
        max-width: 500px;
        justify-content: start;
        align-items: start;
    }
}
</style>