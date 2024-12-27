<script setup lang="ts">
</script>
<template>
    <footer>
       <ul>
              <li><a href="">© 2024 Burn Fitness</a></li>
              <li><a href="">Privacy Policy</a></li>
              <li><a href="">Terms of Service</a></li>
              <li><a href="">Cookie Policy</a></li>
       </ul>
       <ul>
        <li><a href="">Start</a></li>
        <li><a href="#calculator">Calculator</a></li>
        <li><a href="#trainers">Trainers</a></li>
        <li><a href="#memberships">Subscribe</a></li>
       </ul>
         <ul>
          <li><a href="">Facebook</a></li>
          <li><a href="">Instagram</a></li>
          <li><a href="">Twitter</a></li>
          <li><a href="">Youtube</a></li>
        </ul>
    </footer>
</template>
<style scoped>
    footer{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 80px;
        z-index: 40;
        background: #000;
        padding: 0 20px;
        color:#fff;
        font-size: 14px;
    }
    ul{
        list-style: none;
        display: flex;
        padding: 0;
        gap: 20px;
        margin: 0;
        li a{
            cursor: pointer;
            z-index: 10;
            color: #fff;
            text-decoration: none;
        }
        a:hover{
            color: #cf5600;
        }
    }

    @media (max-width: 1024px){
        footer{
            flex-direction: column;
            gap: 20px;
            height: auto;
            padding-bottom: 20px;
            font-size: 12px;
        }
        
    }
</style>