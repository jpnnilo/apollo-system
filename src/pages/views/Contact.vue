<template>
    <div id="Contact">
        <div class="background">
            <div class="container">
                
                <div class="row">
                    <div class="col-lg-6">
                        <img src="/images/light-bulb.jpg" alt="light bulb">
                    </div>
                    <div class="col-lg-6">
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
                </div>
            </div>
        </div>
    </div>
</template>


<script setup lang="ts">
import {ref}  from 'vue'

const title = ref(`Let's do this together.`);

const location = ref({
        location: 'Location',
        details: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
})

const contact = ref({
    contact: 'Contact',
    number: '123-456-7890',
    email: 'email@example.com'
})


</script>


<style scoped>
.background{
    background-color: #D8E9A8;
    height: 960px;
    font-family: 'Poppins', sans-serif;
}

h1{
    padding: 90px 40px 20px;
    font-size: 4vmax;
}

h2{
    font-size: 2vmax;
    margin-bottom: 20px;
}

p{
    font-size: 1vmax;
}

img{
    width: 650px;
}


.row{
    padding: 100px 0 ;
}   



.location{
    padding: 50px 50px 10px;
    
}

.contact {
    padding: 50px;
}

@media(max-width: 1399px){

    .row{
        padding: 40px 0 ;
    }  
    img{
        width: 450px;
    }

    .background{
        height: 700px;
    }

    h1{
        padding: 50px 40px 0;
    }
   
}

@media(max-width: 991px){
   img{
    display:block;
    margin: 0 auto;
    width: 400px;
   }
   .background{
        height: 1100px;
    }

    h2{
        font-size: 3vmax;
    }
    p{
        font-size: 1.6vmax;
    }
  
}

@media(max-width: 447px){
    img{
        width: 300px;
   }
}

</style>