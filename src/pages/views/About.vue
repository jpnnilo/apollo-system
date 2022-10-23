<template>
    <div>
        <div class="background">
            <div class="container">
                <h1>{{ title }}</h1>
                <p>{{ message }}</p>

                <div class="row">
                    <div class="col-lg-4 col-details" v-for="about in abouts" :key="about.title">
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
    background-color: #579b39;
    height: 967px;
}

h1{
    font-family: 'Poppins', sans-serif;
    font-size:4vmax;
    text-align: center;
    padding:100px 0 30px;
    color:white;
}

p{
    display: block;
    margin: 10px auto;
    text-align: center;
    font-size: 1.2vmax;
    color:white;
    font-family: 'Poppins', sans-serif;
}

img{
    width: 150px;
    display:block;
    margin: 5px auto;
    padding: 20px;
}

h2{
    padding: 20px;
    text-align: center;
}


.col-details{
    background-color: #ddffe3;
    height: 500px;
    color:black;
    padding:20px;
    width: 400px;
    margin: 10px;
}


.detail{
    color:black;
    font-size: 1vmax;
}

@media(max-width: 900px){
    p{
    display: block;
    margin: 0 auto;
    width:300px;
    text-align: center;
    font-size: 1.2vmax;
    color:white;
}
}
</style>