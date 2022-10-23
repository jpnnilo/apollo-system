<template>
    <div>
        <div class="background">
            <div class="container">
                <h1>{{ title }}</h1>
                <div class="row">
                    <div class="col" v-for="testimonial in testimonials" :key="testimonial.name">
                        <img :src="testimonial.image" alt="profile">
                        <i class="bi bi-quote"></i>
                        <p>{{ testimonial.message }}</p>
                        <h3 class="name">{{ testimonial.name }}</h3>
                        <h5 class="company">{{ testimonial.position }} at {{ testimonial.company }}</h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script setup lang="ts">
import {ref} from 'vue'

const title = ref('Testimonials');

const testimonials = ref({
    t1: {
        company: 'ABC',
        name: 'John Doe',
        position: 'CEO',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed a libero hendrerit nisi commodo sagittis vitae sit amet tortor. ',
        image: '/images/testimonials/t1.jpg'
    },
    t2: {
        company: 'DEF',
        name: 'Doe John',
        position: 'Manager',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus. ',
        image: '/images/testimonials/t2.jpg'
    },  
    t3: {
        company: 'XYZ',
        name: 'John Lorem',
        position: 'Team Lead',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus. ',
        image: '/images/testimonials/t3.jpg'
    },
})

</script>


<style scoped>

.background{
    background-color: #191A19;
    height: 967px;
     font-family: 'Poppins', sans-serif;
}

h1{
    color: #D8E9A8;
    font-size:4vmax;
    text-align:center;
    padding: 80px 0 10px;
}

.company{
    text-align:center;
    padding: 20px;
}

.name{
    margin: 60px 10px 0;
    display: block;
    text-align: center;

}

.col{
    background-color: #ddffe3;
    margin: 100px 20px 0;
    height: 450px;
    padding: 40px;
    /* box-shadow: 5px 5px 10px #1E5128;  */
}

.bi-quote{
    font-size: 40px;
}

img {
    width: 190px;
    border-radius: 50%;
    display: block;
    margin: -130px auto 0;
    padding: 15px;
    background-color: #191A19;
}


@media(max-width: 991px){
    .background{
        height: 1400px;
    }
  
}

@media(max-width: 768px){
    .background{
        height: 1900px;
    }
  
}



</style>