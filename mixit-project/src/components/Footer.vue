<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>
<div class="contenedor-footer">
    <div class="first-part">
        <div class="logo-aboutus">
            <div class="logo"> 
                <img src="../assets/mixit-logo-bw.jpeg" alt="Logo">
            </div>
            <p>Nosotros cuidamos de tu piel</p>
        </div>
        <div class="email">
            <p>Sugienos y recibe un discuento de 10%</p>
            <input type="text">
        </div>
        <div class="catalogo-menu">
            <div class="menu">
                <p>Tiendas</p>
                <p>Perfil</p>
                <p>Favoritos</p>
                <p>Cesta</p>
            </div>
            <div class="ayuda">
                <p>Contactanos</p>
            </div>
            <div class="tienda">
                <p>Catalogo</p>
                <p>Mujer</p>
                <p>Hombre</p>
                <p>Niño</p>
                <p>Regalos</p>
                <p>Descuentos</p>
                <p>Revistas</p>
            </div>
        </div>
    </div>
    <hr>
    <div class="second-part">
        <div class="rights">All rights are reserved</div>
        <div class="social-media">
            facbook
            twitter
            instagram
        </div>
    </div>
</div>

</template>

<style>
.contenedor-footer{
    background-color: black;
}

.first-part{
    display: flex;
    flex-direction: row;
    color: white;
}

.logo-aboutus{
    width: 20%;
    display: flex;
    flex-direction: column;
}

.logo-aboutus .logo{
    display: flex;
    filter: invert(100%);
    width: 150px;
}

.logo-aboutus .logo img{
    width: 100%;
}

hr{
    height: 1px;
    background-color: rgba(245, 245, 245, 0.452);
    border: none;
    width: 90%;
}
</style>