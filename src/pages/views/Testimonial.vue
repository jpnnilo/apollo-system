<template>
    <div id="Testimonial">
        <div class="background">
            <div class="container">
                <h1>{{ title }}</h1>
                <div class="row details" data-aos="fade-right" data-aos-duration="1500">
                    <div class="col">
                        <h2><i class="bi bi-quote"></i></h2>
                        <h3>{{ message }}</h3>
                        <img :src="profile" alt="profile" >
                        <h4>{{ name }}, {{ position }} @ {{ company }}</h4>  
                    </div>
                </div>
                <div class="row">
                    <div class="col-lg-3 img" data-aos="fade-up" data-aos-duration="1500" v-for="client in clients" :key="client.name" @click="view(client.name, client.company, client.position, client.message, client.profile)">
                        <img :src="client.logo" alt="client logo" >
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script setup lang="ts">
import {ref} from 'vue'

const title = ref('Testimonials');

const clients = ref({
    client1: {
        company: 'Aquabest',
        name: 'John Doe',
        position: 'CEO',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed a libero hendrerit nisi commodo sagittis vitae sit amet tortor. Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
        profile: '/images/clients/t1.jpg',
        logo: '/images/clients/aquabest.png',
    },
    client2: {
        company: 'Calayan',
        name: 'Doe John',
        position: 'Manager',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus.  Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
        profile: '/images/clients/t2.jpg',
        logo: '/images/clients/calayan.png',
    },  
    client3: {
        company: 'Unilever',
        name: 'John Lorem',
        position: 'Team Lead',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus. consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus.',
        profile: '/images/clients/t3.jpg',
        logo: '/images/clients/unilever.png',
    },
    client4: {
        company: 'Hayabusa',
        name: 'John Lorem',
        position: 'Team Lead',
        message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus. ',
        profile: '/images/clients/t3.jpg',
        logo: '/images/clients/hayabusa.png',
    },
})

let name = ref('John Doe');
let company = ref('Aquabest');
let position = ref('CEO');
let message = ref('Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus.  Lorem ipsum dolor sit amet, consectetur adipiscing elit.');
let profile = ref('/images/clients/t1.jpg');

function view(fName:string, fCompany:string, fPosition:string, fMessage:string, fProfile:string){
    name.value = fName;
    company.value = fCompany;
    position.value = fPosition;
    message.value = fMessage;
    profile.value = fProfile;
}

</script>


<style scoped>

.background{
    background-color: #F2F2F2;
    height: 967px;    
    font-family: 'Montserrat', sans-serif;
    color: #2A3539;

}

h1{
    font-size:3vmax;
    text-align:center;
    padding: 80px 0 10px;
    font-weight: 600;
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



.img{
    cursor: pointer;
}

.img img{
    display: block;
    margin: 0 auto;
    width: 200px;
    opacity: .5;   
    
}

.img:hover img{
    opacity: 1;
}

.details{
    padding: 50px;
    border-style: solid;
    background-color: white;
    border-radius: 10px;
    height: 500px;
    width: 1000px;
    margin: 0 auto;
    margin-bottom: 50px;
}

.details img{
    border-radius: 50%;
    width: 100px;
    display: block;
    margin: 50px auto 20px;
}

.details h4{
    display: block;
    margin: 20px auto;
    text-align: center;
}


/* img {
    width: 190px;
    border-radius: 50%;
    display: block;
    margin: -130px auto 0;
    padding: 15px;
    background-color: #191A19;
} */


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