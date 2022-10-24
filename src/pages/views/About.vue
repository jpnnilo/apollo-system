<template>
    <div id='About'>
        <div class="background">
            <div class="container">
                <h1>{{ title }}</h1>
                <p>{{ message }}</p>

                <div class="row">
                    <div class="col col-details" v-for="about in abouts" :key="about.title" >
                        <img :src="about.image" alt="">
                        <h2>{{ about.title }}</h2>
                        <p class="detail">{{ about.message }}</p>
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'

const title = ref('Who We Are?');
const message = ref('The company was established in 1987 to cater the need of the construction industry which was booming then. Seeing the high demand for our products by our satisfied customers, the company decided that aside from having it locally purchased, it will also venture in the important of these products abroad to give a wide array of designs with prices much affordable by our customers who has been patronizing our products for the longest time');


const abouts = ref({
    mission: {
        title: 'Mission',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed a libero hendrerit nisi commodo sagittis vitae sit amet tortor. ',
        image: '/icons/002-mission.png'
    },
    vision: {
        title: 'Vision',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus. ',
        image: '/icons/001-shared-vision.png'
    },  
    goal: {
        title: 'Goal',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus. ',
        image: '/icons/003-goal.png'
    },
})


</script>

<style scoped>

.background{
    background-color: #1E5128;
    height: 900px;
}

h1{
    font-family: 'Poppins', sans-serif;
    font-size:3.5vmax;
    text-align: center;
    padding: 70px 0 30px;
    color: #D8E9A8;
}

p{
    
    text-align: center;
    font-size: 1vmax;
    color: #D8E9A8;
    font-family: 'Poppins', sans-serif;
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

.row{
    margin: 0 auto;
}

.col-details{
    
    background-color: #191A19;
    margin: 40px 20px 0;
    height: 400px;
    padding: 20px;
    border-radius: 10px;
    /* box-shadow: 5px 5px 10px #D8E9A8; */
    color: #D8E9A8;
}


.detail{
    color: #D8E9A8;
    font-size: 1vmax;
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