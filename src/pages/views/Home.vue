<template>
    <div id="Home">
        <div class="background">
            <div class="container">
                <div class="row">
                    <div class="col" >
                        <h1>{{ company }}</h1>
                        <p>{{ line.first }} <span>{{ line.second }}</span> </p>
                        <div class="button">
                            <Button :text=text />
                        </div>
                    </div>
                    <div class="col">
                        <img src="/images/admin-panel/dashboard.png" alt="dashboard">
                    </div>
                </div>
            </div>
        </div>
    </div>  
</template>


<script setup lang="ts">
import {ref} from 'vue';
import Button from '../../components/Button.vue'

const company = ref('Apollo Systems');
const line = ref({
    first :'we specialize in creating web and mobile applications to improve your',
    second: 'business  operations',
});
const text = "Learn more!"; 

</script>


<style scoped>

h1{
    font-family: 'Montserrat', sans-serif;
    font-weight: 900;
    font-size:4.5vmax;
    margin: 200px auto 50px;
    padding-top:30px;
    color:#10B981;
}

.background{
    height: 910px;
    background-color: #2A3539;
}

img{
    width: 750px;
    display:block;
    margin: 200px auto;
    /* background-color: #1BBBA4; */
    background-color: #10B981;
    padding: 20px;
}

p{  
    font-weight: 600;
    font-size: 1.1vmax;
    margin: 50px 0;
    font-family: 'Montserrat', sans-serif;
    color:white;
    /* color:#10B981; */
}

span{
    font-size: 1.1vmax;
    font-family: 'Montserrat', sans-serif;
    color:#10B981; 
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