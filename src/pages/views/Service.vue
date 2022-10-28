<template>
    <div id="Services">
        <div class="background">
            <div class="container">
                <h1>{{ title }}</h1>
                <p>{{ desc }}</p>
                <div class="row" >
                    <div class="col-lg-6">
                        <div class="row" >
                            <div class="col-lg-6" v-for="service in services" :key="service.title">
                                <div class="services"  @click="select(service.desc, service.title)" data-aos="fade-up" data-aos-duration="2000">
                                    <img :src="service.image" :alt="service.title" >
                                    <h5 >{{ service.title }}</h5>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-6 desc" data-aos="fade-up" data-aos-duration="2000">
                        <h2>{{ titleServices }}</h2>
                        <h5 v-for="desc in arrDesc" >{{ desc }}</h5>
                    </div>
                </div>  
            </div>
        </div>
    </div>
</template>
<script setup lang="ts">
import { isReactive, ref, computed } from 'vue'
import { object } from 'zod';


const title = ref('Services');

const desc = ref('All of these services are customizable to cater to your business needs');

const services = ref({
    pos: {
        title: 'Point of sales',
        desc: ['- Records and processes sales transactions', '- Automatically updates sales and inventory accounts'],
        image: '/icons/002-point-of-sale.png',
        bool: true,
    },
    warehouse: {
        title: 'Warehouse/Inventory',
        desc: ['-Tracks all inventory movements for updated and accurate inventory counts', '- Records accountable person and documents transactions for risk reduction aon theft'],
        image: '/icons/005-inventory.png',
        bool: false,
    },
    payroll: {
        title: 'HR/Payroll',
        desc: ['- Manages employee records', '- Reports employee performance and needs'],
        image: '/icons/007-salary.png',
        bool: false,
    },
    accounting: {
        title: 'Accounting',
        desc: ['- Monitorrs cash, sales, expenses, recievables, loans, and liquadation movements.','- Provide more accure and specific reports and data comparison'],
        image: '/icons/003-accounting.png',
        bool: false,
    },
    website: {
        title: 'Website Application',
        desc: ['-Fully functional websites',
            '- Design with features like simple product selling',
            '- Reflective of your corporate identity'],
        image: '/icons/004-internet.png',
        bool: false,

    },
    mobile: {
        title: 'Mobile Application',
        desc: ['- Serve your customers', '- Connect with your employee','-reach new clients'],
        image: '/icons/001-app-development.png',
        bool: false,
    },
    
})


let titleServices = ref('Point of sales');

let arrDesc = ref(['- Records and processes sales transactions', '- Automatically updates sales and inventory accounts']);
let isActive = ref(true);

const classObject = computed(() => ({
  active: isActive.value = true
}))


function select(desc: string[], title: string){
    console.log(desc);
    // arrSelected.value = selected;
    arrDesc.value = desc;
    titleServices.value = title;
}


</script>

<style scoped>
.background {
    display: block;
    margin:0 auto;
    border-radius: 20px;
    width: 1400px;
    height: 900px;
    /* background-color: #F2F2F2; */
    background-color: #10B981;
    font-family: 'Montserrat', sans-serif;
    color:white;
    font-weight: 600;
    margin-bottom: 70px;
    
    box-shadow: 2px 2px 10px #3a2f2f;
}


h1 {
    color:white;
    font-weight: 600;
    font-size: 3.5vmax;
    text-align: center;
    padding: 50px 0 20px;
}




.services h5{
    text-align:center;
    cursor: pointer;
}

p{

    color:white;
    text-align: center;
    font-size: 1vmax;
    font-weight: 600;
}

.services{
    cursor:pointer;
}

img {
    display: block;
    margin: 50px auto 10px;
    padding: 10px;
    width: 100px;
    border-radius: 50%;
    background-color: white;
    opacity: 0.6;   
}

.services:hover img{
    box-shadow: 2px 2px 10px #8f7474;
    opacity: 1;   
}

.servicesHover{
    box-shadow: 2px 2px 10px #8f7474;
    opacity: 1;   
}



.desc{
    padding: 130px 20px 0 0;
}

.desc h2{
    text-align: center;
    font-weight: 600;
    margin: 50px 0;
}

.desc h5{
    font-weight: 600; 
}


@media(max-width: 991px){
    .background{
        height: 1200px;
    }
    img {
        width: 70px;
        margin: 10px auto 0;
    }
    .service{
        /* box-shadow: 2px 2px 10px gray; */
        margin: 10px;
        height: 300px;
    }
}

@media(max-width: 767px){
    .background{
        height: 2100px;
    }
   
}

</style>