<template>
    <div>
        <div class="background">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <h1>{{ company }}</h1>
                        <p>{{ line }}</p>
                        <div class="button">
                            
                            <Button :text=text />
                        </div>
                    </div>
                    <div class="col">
                        <img src="/images/light-bulb.jpg" alt="light bulb">
                    </div>
                </div>
            </div>
        </div>
    </div>  
</template>


<script setup lang="ts">
import {ref} from 'vue';
import Button from '../../components/Button.vue'

const company = ref('Apollo System');
const line = ref('we specialize in creating web and mobile applications to improve your business  operations');
const text = "Learn more!"; 

</script>


<style scoped>

h1{
    font-family: 'Cormorant Garamond', serif;
    font-size:4.5vmax;
    margin: 200px auto 50px;
    padding-top:30px;
}

.background{
    height: 910px;
    background-color: #191A19;
    color: #D8E9A8;

}

img{
    width: 550px;
    display:block;
    margin: 100px auto;
    background-color: #1E5128;
    padding: 20px;
}

p{
    font-size: 1.1vmax;
    margin: 50px 0;
    font-family: 'Poppins', sans-serif;
}


@media(max-width: 1100px){
    
    .background{
        height:650px;
    }
    img{
        width: 400px;
        margin: 100px auto;
        background-color: #579b39;
        padding: 10px;
    }
}

@media(max-width: 769px){

    h1{
        text-align: center;
        margin: 50px 0 20px;
    }
    p{
        text-align: center;
        margin: 20px 0;
    }

    img{
        margin: 20px auto;
    }


    .background{
        height: 800px;
    }

    .button{
      text-align: center;
    }
}

@media(max-width: 436px){
    
    .background{
        height: 600px;
    }


    img{
        width: 250px;
       
    }
}


</style>