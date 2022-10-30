<template>
    <div id='About'>
        <div class="background">
            <div class="container" data-aos="zoom-in" data-aos-duration="1500">
                <h1>{{ title }}</h1>
                <p>{{ message }}</p>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'

const title = ref('What Apollo has to offer?');
const message = ref('Apollo Systems is a product of our pursuit to continually improve business operations. We developed web-based systems that provide us with real-time, reliable, and organized data making our operations fast and efficient. We are now committed to deliver the same value to you.');



</script>

<style scoped>

.background{
    background-color: white;
    height: 220px;
    
    font-family: 'Montserrat', sans-serif;
}

h1{
    font-size:2vmax;
    text-align: center;
    padding: 0 0 30px;
    color: black;
    font-weight: 600;
}

p{
    
    text-align: center;
    font-size: 1vmax;
    color: black;
}

img{
    width: 100px;
    display:block;
    margin: 5px auto;
    padding: 5px;
    background-color: #4E9F3D;
    border-radius: 50%;
}

h2{
    padding: 20px;
    text-align: center;
}


@media(max-width: 769px){
    .col-details{
        
        height: 380px;
    }

    .background{
        height: 1200px;
    }

}

@media(max-width: 498px){
    .col-details{
        margin:5px 5px;
        padding: 5px;
        height: 310px;
    }
    .background{
        height: 1000px;
    }

}

@media(max-width: 379px){
    .background{
        height: 1000px;
    }

} 

@media(max-width: 379px){
    .background{
        height: 1300px;
    }
} 


</style>