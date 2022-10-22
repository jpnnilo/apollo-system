<template>
    <div>
        <button type="button" class="btn btn-outline-success">{{ text }}</button>
    </div>
</template>


<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps(['text']);


</script>


<style scoped>

button{
    border-radius: 0;
    font-size:1vmax;
}

</style>
