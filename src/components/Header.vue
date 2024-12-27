<script setup lang="ts">
import {ref} from 'vue'
let nav =ref<boolean>(false)
function toggleNav() {
    nav.value = !nav.value
}
//changes the value to true or false when the menu is clicked 
// to know if you need the nav open or closed in movil

</script>

<template>
  <header>
    <picture class="logo">
        <img src="./icons/Logo.png" alt="">
    </picture>
    <nav>
    <ul :class="{ shownav: nav }">
        <li @click="toggleNav"><a href="">START</a></li>
        <li @click=""toggleNav><a href="#trainers">TRAINERS</a></li>
        <li @click="toggleNav"><a href="#calculator">CALCULATOR</a></li>
        <li @click="toggleNav"><a href="memberships">SUBSCRIBE</a></li> 
    </ul>
    </nav>
    <picture class="menu" @click="toggleNav">
        <img src="./icons/Menu.svg" alt="">
    </picture>
  </header>
</template>

<style scoped>
    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 80px;
        z-index: 40;
        background: transparent;
        padding: 0 20px;
        font-weight: 800;
        color:#fff;
    }
    ul{
        list-style: none;
        display: flex;
        flex-direction: column;
        gap: 20px;
        position: absolute;
        padding: 40px 0;
        margin: 0;
        text-align: center;
        top: -990px;
        background-color: #000;
        z-index: 40;
        left: 0;
        width: 100%;
        transition: all 300ms ease-in-out;
         li{
            z-index: 10;
            a{
                text-decoration: none;
                color: #fff;
            }
         }

        li:hover{
            color: #cf5600;
        }
    }
    .menu{
        display: block;
        z-index: 45;
        width: 40px;

        img{
            width: 100%;
            cursor: pointer;
        }
    }

    .logo{
    z-index: 45;
    width: 44px;
        img{
        width: 100%;
        }
    }

    .shownav{
        top: 0;
    }


    @media (min-width: 768px) {

        header{
            max-width: 1200px;
            margin: auto;
        }
        ul{
        flex-direction: row;
        position: relative;
        background-color: transparent;
        top: 0;
        li{
            cursor: pointer;
            }
    }
        .menu{
        display: none;
        }
    }
</style>
