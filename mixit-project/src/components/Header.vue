<template>

<div class="contenedor-header">
    <div class="white-part">
        <div class="logo">
            <img src="../assets/mixit-logo.jpeg" alt="">
        </div>
        <input type="search" name="search" id="search">
        <div class="iconos">
            <div class="icon" id="tiendas">
                <p>Tiendas</p>
                <div class="icono-bts"></div>
            </div>
            <div class="icon" id="perfil">
                <p>Perfil</p>
                <div class="icono-bts"></div>
            </div>
            <div class="icon" id="favoritos">
                <p>Favoritos</p>
                <div class="icono-bts"></div>
            </div>
            <div class="icon" id="cesta">
                <p>Cesta</p>
                <div class="icono-bts"></div>
            </div>
        </div>
    </div>
    <div class="black-part">
        <div class="catalogo-decuentos">
            <p class="catalogo">Catalogo</p>
            <p class="decuentos">Descuentos</p>
        </div>
        <div class="contactanos">
            <p class="contactanos">Contactanos</p>
        </div>
    </div>
</div>

</template>

<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>


<style>
.contenedor-header{
    background-color: white;
    height: 120px;
    display: flex;
    flex-direction: column;
    border: 2px red solid;
}

.white-part{
    height: 50%;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.logo{
    display: flex;
    padding: 8px;
    margin-left: 15px;
    width: 15%;
}

.white-part input{
    background-color: blue;
    height: 30px;
    width: 200px;
    margin-left: 20px;
    margin-right: 20px;
}

.iconos{
    width: 50%;
    display: flex;
    flex-direction: row;  
    justify-content: space-between; 
    background-color: blueviolet; 
    
}

.icon{
    background-color: aqua;
}

.black-part{
    background-color: black;
    display: flex;
    flex-direction: row;
}
</style>
