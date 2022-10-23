<template>
    <div>
        <div class="background">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <h1>{{ company }}</h1>
                        <p>{{ line }}</p>
                        <Button :text=text />
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
    background-color: #ddffe3;

}

img{
    width: 550px;
    display:block;
    margin: 100px auto;
    background-color: #579b39;
    padding: 20px;
}

p{
    font-size: 1.1vmax;
    margin: 50px 0;
    font-family: 'Poppins', sans-serif;
}


@media(max-width: 900px){
    h1{
        margin: 50px 0;
    }

    img{
    width: 300px;
    margin: 100px auto;
    background-color: #579b39;
    padding: 10px;
}

}
</style>