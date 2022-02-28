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
            <button class="catalogo">Catalogo</button>
            <button class="decuentos">Descuentos</button>
        </div>
        <button class="contactanos">
            <p class="contactanos">Contactanos</p>
        </button>
    </div>
</div>

</template>

<script setup>
import { ref } from 'vue'
import bootstrap from 'bootstrap'
import { mdiAccount } from "@mdi/js";

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
    position: static;
}

.white-part{
    height: 50%;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    color: black;
}

.logo{
    display: flex;
    padding: 8px;
    margin-left: 15px;
    width: 15%;
}

.white-part input{
    height: 30px;
    width: 200px;
    margin-left: 20px;
    margin-right: 20px;
    align-self: center;
}

.iconos{
    width: 50%;
    display: flex;
    flex-direction: row;  
    justify-content: space-between; 
}

.icon{
    display: flex;
    flex-direction: row;
    border: 2px blue solid;
}

.icono-bts{
    border: 2px tomato solid;
    display: flex;
    align-self: center;
}

.black-part{
    background-color: black;
    display: flex;
    flex-direction: row;
    color: white;
    justify-content: space-between;
    padding-left: 20px;
    padding-right: 20px;
}

.black-part button{
    margin-top: 5px;
    margin-bottom: 5px;
    background-color: black;
    border-radius: 7px;
    color: white;
    border: none;
}

.black-part button:hover{
    background-color: white;
    color: black;

}

.catalogo-decuentos{
    display: flex;
    flex-direction: row;
    width: 50%;
    flex-direction: row;
    justify-content: left;
}

.catalogo-decuentos button{
    margin-right: 20px;
}


</style>
