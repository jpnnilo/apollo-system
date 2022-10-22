<template>
    <div>
        <div class="background">
            <div class="container">
                <h1>{{ title }}</h1>
                <p>{{ message }}</p>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'

const title = ref('Who We Are?');
const message = ref('Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar lacus sit amet tellus lobortis finibus. Integer feugiat aliquet felis non rhoncus. Nulla facilisi. Quisque porta purus id elit pharetra placerat. Donec nec enim cursus, ultricies leo sed, euismod sem. In sem elit, tempus ac fringilla eu, cursus finibus orci. Suspendisse tincidunt, felis at tristique scelerisque, turpis velit porttitor purus, et gravida mi nisl vel mi. Nulla ornare leo ultricies nulla posuere, interdum tempor sem ultricies. Cras sed orci a nunc condimentum aliquam. Praesent fermentum sapien fermentum eros pellentesque porta. Donec suscipit orci a mi efficitur, id mollis quam mollis. Suspendisse ac ultrices urna. Ut porttitor ipsum ac dolor porttitor vulputate.');



</script>

<style scoped>

.background{
    background-color: #579b39;
    height: 967px;
}

h1{
    font-family: 'Cormorant Garamond', serif;
    font-size:4.5vmax;
    text-align: center;
    padding:150px 0 70px;
    color:white;
}

p{
    display: block;
    margin: 0 auto;
    width:1000px;
    text-align: center;
    font-size: 1.2vmax;
    color:white;
}

img{
    width: 600px;
    display:block;
    margin: 20px auto;
    background-color: #a4f87f;
    padding: 20px;
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