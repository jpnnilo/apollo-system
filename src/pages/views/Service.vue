<template>
    <div>
        <div class="background">
            <div class="container">
                <h1>Services</h1>
                <div class="row services">
                    <div class="col-lg-6 " v-for="service in services" :key="service.title">
                        <div class="row">
                            <div class="col-lg-4">
                                <img :src="service.image" :alt="service.title">
                            </div>
                            <div class="col-lg-8">
                                <h2>{{ service.title }}</h2>
                                <h5 v-for="desc in service.desc"> {{ desc }} </h5>
                            </div>
                        </div>
                    </div>
                </div>  
            </div>
        </div>
    </div>
</template>
<script setup lang="ts">
import { ref } from 'vue'

const services = ref({
    pos: {
        title: 'Point of sales',
        desc: ['-records and processes sales transactions', '-automatically updates sales and inventory accounts'],
        image: '/icons/002-point-of-sale.png'
    },
    warehouse: {
        title: 'Warehouse/Inventory',
        desc: ['-tracks all inventory movements for updated and accurate inventory counts', '-records accountable person and documents transactions for risk reduction aon theft'],
        image: '/icons/005-inventory.png'
    },
    payroll: {
        title: 'HR/Payroll',
        desc: ['-manages employee records', '-reports employee performance and needs'],
        image: '/icons/007-salary.png'
    },
    website: {
        title: 'Website Application',
        desc: ['-fully functional websites',
            '-design with features like simple product selling',
            '-reflective of your corporate identity'],
        image: '/icons/004-internet.png'

    },
    mobile: {
        title: 'Mobile Application',
        desc: ['-serve your customers', '-connect with your employee','-reach new clients'],
        image: '/icons/001-app-development.png'
    },
    accounting: {
        title: 'Accounting',
        desc: ['-monitorrs cash, sales, expenses, recievables, loans, and liquadation movements.','-provide more accure and specific reports and data comparison'],
        image: '/icons/003-accounting.png'
    },
})

</script>

<style scoped>
.background {
    height: 960px;
    background-color: #ddffe3;
}


h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 4.5vmax;
    text-align: center;
    padding: 60px 0 0;
}

h2 {
    margin: 20px auto;
    width:400px;
}

img {
    width: 70px;

    display: block;
    margin: 70px auto 0;
}

.services{
    margin-top: 70px;
}

</style>