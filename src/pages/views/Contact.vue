<template>
    <div id="Contact">
        <div class="layer1 spacer"></div>
        <div class="background">
            <div class="container">
                <div class="row">
                    <div class="col-lg-6" data-aos="fade-right" data-aos-duration="1500">
                        <h1>{{ title }}</h1>
                        <div class="location">
                            <h2>{{ location.location }}</h2>
                            <p>{{ location.details }}</p>
                        </div>
                        <div class="contact">
                            <h2>{{ contact.contact }}</h2>
                            <p>{{ contact.number }}</p>
                            <p>{{ contact.email }}</p>
                        </div>
                    </div>
                    <div class="col-lg-6 form" data-aos="fade-left" data-aos-duration="1500">
                        <form>
                            <h2>Get in Touch</h2>
                            <Input :label="`Name`" :placeholder="`Enter your name`"></Input>
                            <Input :label="`Email`" :placeholder="`Enter your email address`"></Input>
                            <Input :label="`Phone`" :placeholder="`Enter your phone number`"></Input>
                            <Input :label="`Message`" :placeholder="`Enter your message`"></Input>
                            <Button :text="`Submit`"></Button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script setup lang="ts">
import { ref } from 'vue'
import Input from '../../components/Input.vue'
import Button from '../../components/Button.vue'

const title = ref(`Contact Us`);

const location = ref({
    location: 'Location',
    details: `Suite 3003-A East Tower, PSE Center Exchange Road, Ortigas Center Pasig`,
})

const contact = ref({
    contact: 'Contact',
    number: `T: 632 687-7111 loc 88`,
    email: `inquiry@apollosystems.ph`
})


</script>


<style scoped>
.background {
    background-color: #2A3539;
    height: 700px;
    font-family: 'Montserrat', sans-serif;
}

h1 {
    padding: 90px 40px 20px;
    font-size: 3vmax;
    color: #10B981;
    text-align: center;
    font-weight: 600;
}
h2{
    color: #10B981;
}

p{
    color: white;
}

.location{
    padding:0 20px;
    margin: 50px 0 ;
}

.contact{
    padding:0 20px; 
    margin: 50px 0 ;
}

.form{
    margin: 35px 0;
    background-color: white;
    padding: 70px 80px ;
}

.form h2{
    font-weight: 600;
    margin: 20px 0;
}

Button{
    margin-top: 100px;
}

.spacer{
    aspect-ratio: 960/100;
    background-size:cover;
    
}

.layer1{
    background-image: url('/svg/contact-layer.svg');
}

@media(max-width: 1399px) {

    .row {
        padding: 40px 0;
    }

    img {
        width: 450px;
    }

    .background {
        height: 700px;
    }

    h1 {
        padding: 50px 40px 0;
    }

}

@media(max-width: 991px) {
    img {
        display: block;
        margin: 0 auto;
        width: 400px;
    }

    .background {
        height: 1100px;
    }

    h2 {
        font-size: 3vmax;
    }

    p {
        font-size: 1.6vmax;
    }

}

@media(max-width: 447px) {
    img {
        width: 300px;
    }
}
</style>