<script setup>
import {achievements} from '../assets/data/data.js'
  import Header from '../components/Header.vue'
</script>
<template>
    <section class="hero_container">
        <Header/>
        <div class="hero">
        <div class="hero_texts">
            <h1>Transform Your Fitness  Journey Today!</h1>
            <p>Discover personalized workouts, expert tips, and the motivation
                you need to achieve your goals. <span class="orange">Your best self starts here</span></p>
                <button>START TODAY</button>
        </div>
        <picture class="model">
            <img src="/multimedia/women-flexing.png" alt="">
        </picture>
        <ul class="achievements">
        <li v-for="data in achievements"><span class="achievement-many">{{data.many}}</span><br/><span class="achievement-name">{{data.name}}</span></li>
        </ul>
    </div>
        <div class="hero_background">
        </div>
    </section>

</template>
<style scoped>

.hero{
    max-width: 1200px;
    margin: auto;
    padding: 0px 20px;
}

.hero_texts,.achievements{
    position: absolute;
    z-index: 15;
    color: #fff;
}

.model{
    position: absolute;
    z-index: 10;
    right: 0;
    bottom: 0;
}

.achievements{
    bottom: 0;
    display: flex;
    flex-direction: column;
    list-style: none;
    gap: 20px;
    padding: 0;
    li{
        text-align: center;
    }
}

.achievement-name{
    color: #cf5600;
    text-transform: uppercase;
    font-size: 20px;
    font-weight: 600;
}

.achievement-many{
    font-size: 26px;
    font-weight: 800;
}

.hero_texts{
    max-width: 600px;
    text-wrap: balance;
    h1{
       font-size: 24px;
       margin-bottom: 0;
    }
    p{
        margin-top: 4px;
    font-size: 16px;
    }
}
    .hero_container{
        height: 100vh;
        max-height: 800px;
        position: relative;
    }

    .hero_background{
        position: relative;
        width: 100%;
        height: 100%;
        max-height: 800px;
        z-index: 5;
        position: absolute;
        top: 0px;
        background:url('/multimedia/train-bg.jpg');
        background-size: cover;
        background-position: start;
        filter: brightness(17%);
    }

    .model{
            max-width: 200px;
            img{
                width: 100%;
            }
        }

    @media (min-width: 425px) {
        .model{
            max-width: 250px;
        }
        .achievement-name{
    font-size: 24px;
        }

        .achievement-many{
            font-size: 30px;
        }
        .hero_texts{
            h1{
       font-size: 28px;
    }
        }
   

    }

    @media (min-width: 956px) {
        .hero_texts h1{
        font-size: 55px;   
        }

        .hero_texts p{
            font-size: 20px;
            margin-top: 10px;
        }

        .model{
            max-width: 380px;
        }
        .achievements{
            flex-direction: row;
            gap: 40px;
            bottom: 10px;
        }
        .achievement-name{
    font-size: 24px;
        }

        .achievement-many{
            font-size: 50px;
        }

    }




</style>