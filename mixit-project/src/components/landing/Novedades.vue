<script setup>
import { ref } from 'vue'
import Offer from './Offer.vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>
    <div class="contenedor-novedades">
        <Offer></Offer>
    </div>
</template>


<style>
.contenedor-novedades{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
</style>