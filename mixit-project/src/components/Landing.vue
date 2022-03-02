<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>
  <div class="contenedor-ofertas">
    <div class="flechas">
      <img src="../assets/arrow-left-circle.svg" alt="">
      <img src="../assets/arrow-right-circle.svg" alt="">
    </div>
    <div class="image">
      <img src="../assets/offer1.png" alt="">
    </div>
  </div>
</template>

<style>
.contenedor-ofertas{
  height: 700px;
  /* border: 2px fuchsia solid; */
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
}

.image{
  height: 100%;
  width: 100%;
  display: flex;
  overflow: hidden;
  border: 2px hotpink solid;
}

.image img{
  /* width:100%; */
  /* height:800px;  */
  display: flex;
  background-color: hotpink;
}

.flechas{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 98%;
  position: absolute;
}

.flechas:hover{
  cursor: pointer;
}

.flechas img{
  height: 35px;
  width: 35px;
}

.image img{
  display: flex;
  height: 600px;
  width: 100%;
  zoom: 0.9;
}
</style>