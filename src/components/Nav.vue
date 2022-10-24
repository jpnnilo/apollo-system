<template>
    <div>
        <div class="background">
            <div class="container">
                
                <nav class="navbar navbar-expand-lg">
                    <div class="container-fluid">
                        <i class="bi bi-triangle-half"></i>
                        <a class="navbar-brand" href="#Home">{{ title }}</a>
                        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                        </button>
                        <div class="collapse navbar-collapse" id="navbarNavDropdown">
                            <ul class="navbar-nav">
                                
                                <li class="nav-item" v-for="nav in navs" :key="nav">
                                    <a class="nav-link" :href="`#${ nav }`">{{ nav }}</a>
                                </li>
                                
                               
                            </ul>
                        </div>

                        <div class="collapse navbar-collapse justify-content-end" id="navbarNavDropdown">
                            <ul class="navbar-nav ">
                            <li class="nav-item" v-for="social in socials" :key="social">
                                <a class="nav-link" href="#"><i class="bi" :class="'bi-' + social"></i> </a>
                                
                            </li>
                        </ul>
                        </div>
                    </div>
                </nav>
            
            </div>
        
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const title = ref('Apollo');

const navs = ref({
    about: 'About',
    services: 'Services',
    testimonial: 'Testimonial',
    contact: 'Contact',
});

const socials = ref({
    fb: 'facebook',
    ig: 'instagram',
    twitter: 'twitter',
});


</script>


<style scoped>

.background{
    background-color: #D8E9A8;
    font-family: 'Poppins', sans-serif;
    color: #191A19;
}

.nav-item{
    padding:10px;
    font-size: 1vmax;
    cursor: pointer;
}

</style>