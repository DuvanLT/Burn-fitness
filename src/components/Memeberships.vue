<script setup lang="ts">
</script>
<template>
    <div class="memeberships_container" id="memberships">
    <h3>MEMEBERSHIPS</h3>
    <div class="pricing_container">
        <div class="pricing">
            <div class="card">
                <h4>Baby Builder</h4>
                <h5 class="orange">$9</h5>
                <h6 class="orange">per 1 mounth</h6>
                <ul class="features">
                    <li>Dumbell zone</li>
                    <li>Cardio zone</li>
                    <li>Free water</li>
                </ul>
                <button>Buy now</button>
            </div>
            <div class="card middle">
                <h4>Dumbell maker</h4>
                <h5 class="orange">$45</h5>
                <h6 class="orange">per 4 mounth</h6>
                <ul class="features">
                    <li>Dumbell zone</li>
                    <li>Cardio zone</li>
                    <li>Own trainer</li>
                    <li>Free water</li>
                </ul>
                <button>Buy now</button>
            </div>
            <div class="card">
                <h4>Bench Destroyer</h4>
                <h5 class="orange">$80</h5>
                <h6 class="orange">per 1 year</h6>
                <ul class="features">
                    <li>Dumbell zone</li>
                    <li>Cardio zone</li>
                    <li>Own top trainer</li>
                    <li>Free water</li>
                    <li>Pose room</li>
                </ul>
                <button>Buy now</button>
            </div>
            
        </div>
    </div>
</div>
</template>
<style scoped>
.memeberships_container{
    display: flex;
    flex-direction: column;
    background: #000;
    padding: 20px;
}
.pricing_container{
    max-width: 1200px;
    margin: auto;
}
.pricing{
        color: #fff;
        display: flex;
        flex-direction: column;
        gap: 30px;
    }
h3{
    font-size: 36px;
    color: #cf5600;
}

.card{
    border: #fff solid 3px;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 150px;
    height: 400px;
    padding: 40px;
    h4{
        font-size: 24px;
        margin: 0;
    }
    h5{
        font-size: 40px;
        margin: 10px 0px;
    }
    h6{
        font-size: 14px;
        margin: 10px 0px 40px 0px;
    }
    

}
.features{
    text-align: center;
    padding: 0;
    list-style: none;
}

@media (min-width: 768px){
    .pricing{
        flex-direction: row;
        justify-content: center;
        align-items: end;
        padding: 50px;
    }
    .features{
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
    h3{
        padding:  0px 40px;
        margin-bottom: 0;
    }
    .middle{
        border: #cf5600 solid 3px;
        margin-bottom: 40px;
    }
    button{
        padding: 10px 20px;
        background-color: #cf5600;
        color: #fff;
        border: none;
        cursor: pointer;
    }
    button:hover{
        background-color: #fff;
        color: #cf5600;
    }
    .card{
      width:100px;
    }
}

@media (min-width:1024px) {
    .card{
        width: 180px;
    }
}
</style>