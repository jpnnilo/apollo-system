<template>
    <div class="mb-4">
        <label class="form-label">{{ label }}</label>
        <input type="input" class="form-control" :placeholder="placeholder">
    </div>
</template>


<script setup lang="ts">
import {ref} from 'vue';

const props = defineProps({
    label:String,
    placeholder:String,
})

</script>


<style scoped   >


</style>