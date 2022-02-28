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
                <input type="text" placeholder="Your email address">
            </div>
            <div class="catalogo-menu">
                <div class="opciones">
                    <p id="nombre-opciones">MENU</p>
                    <p>Tiendas</p>
                    <p>Perfil</p>
                    <p>Favoritos</p>
                    <p>Cesta</p>
                </div>
                <div class="opciones">
                    <p id="nombre-opciones">AYUDA</p>
                    <p>Contactanos</p>
                </div>
                <div class="opciones">
                    <p id="nombre-opciones">TIENDA</p>
                    <p>Catalogo</p>
                    <p id="catalogo">Mujer</p>
                    <p id="catalogo">Hombre</p>
                    <p id="catalogo">Niño</p>
                    <p id="catalogo">Regalos</p>
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
    font-family: Avenir, Helvetica, Arial, sans-serif;;
}

.first-part{
    display: flex;
    flex-direction: row;
    color: white;
    justify-content: space-between;
}

.logo-aboutus{
    width: 20%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    margin-left: 10px;
}

.logo-aboutus .logo{
    display: flex;
    filter: invert(100%);
    width: 170px;
    align-content: center;
    align-items: center;
    /* border: 2px blue solid; */
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

.catalogo-menu{
    display: flex;
    width: 45%;
    justify-content: space-between;
    padding-top: 10px;
}

.email{
    display: flex;
    flex-direction: column;
    padding: 20px;
    justify-content: center;
}

.email input{
    background: rgba(253, 253, 253, 0.199);
    height: 50px;
    border: none;
    border-radius: 5px;
    padding-left: 20px;
    font-size: 16px;
    color: white;
    font-family: Avenir, Helvetica, Arial, sans-serif;;
}

.email input::placeholder{
    font-size: 16px;
    font-family: Avenir, Helvetica, Arial, sans-serif;;
}

.opciones{
    width: 100%;
}

.opciones p{
    text-align: left;
    color: rgba(255, 255, 255, 0.712);
}

.opciones p:hover{
    color: white;
    zoom: 1.2;
}

#nombre-opciones{
    text-align: center;
    font-style: bold;
    color: white;
}

#catalogo{
    padding-left: 30px;
}

.second-part{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 20px 40px 30px 40px;
    color: rgba(255, 255, 255, 0.644);
}

</style>