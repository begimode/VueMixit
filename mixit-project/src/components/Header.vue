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
                <div class="icono-bts">
                    <img src="../assets/geo-alt.svg" alt="" id="icono-vacio">
                    <img src="../assets/geo-alt-fill.svg" alt="" id="icono-fill">
                </div>
            </div>
            <div class="icon" id="perfil">
                <p>Perfil</p>
                <div class="icono-bts">
                    <img src="../assets/person.svg" alt="" id="icono-vacio">
                    <img src="../assets/person-fill.svg" alt="" id="icono-fill">
                </div>
            </div>
            <div class="icon" id="favoritos">
                <p>Favoritos  </p> 
                <div class="icono-bts">
                    <img src="../assets/heart.svg" alt="" id="icono-vacio"> 
                    <img src="../assets/heart-fill.svg" alt="" id="icono-fill">
                </div>
            </div>
            <div class="icon" id="cesta">
                <p>Cesta</p>
                <div class="icono-bts">
                    <img src="../assets/cart.svg" alt="" id="icono-vacio">
                    <img src="../assets/cart-fill.svg" alt="" id="icono-fill">
                </div>
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
// import bootstrap from 'bootstrap'

defineProps({
  msg: String
})


// $('.icon').hover(function(){
//   $('#icono-fill').css({
//     "zoom": "2", 
//   });
// });

// document.getElementById('tiendas').addEventListener("mouseenter", function(event){
    // event.target.style.color = "red";
    // setTimeout(function(){
    //     event.target.style.color = "green";
    // }, 1000)
// }, false)


// .hover(function(){
//     $document.getElementById('icono-vacio').css({
//         "zoom": "2"
//     })
// })

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
    /* border: 2px blue solid; */
    height: 80%;
    align-items: center;
    align-self: center;
}

.icono-bts{
    /* border: 2px tomato solid; */
    display: flex;
    height: 25px;
    width: 25px;
    align-self: center;
    justify-content: center;
    align-content: center;
    align-items: center;
    margin-left: 2px;
    margin-right: 5px;
    margin-bottom: 5px;
}

.icono-bts img{
    height: 100%;
    width: 100%;
    overflow: hidden;
}

#icono-vacio{
    z-index: 10;
    background-color: white;
    /* transition: all 0.5s ease-in-out; */
}

#icono-fill{
    position: absolute;
    width: 25px;
    height: 25px;
    /* transition: all 0.5s ease-in-out; */
    /* visibility: visible; */
    z-index: 7;
}

#icono-fill:hover{
    visibility: visible;
    /* transition: all 0.5s ease-in-out; */
    /* transition-duration: 1s; */
}


#icono-vacio:hover{
    visibility: hidden;
    /* transition: all 0.5s ease-in-out; */
    /* transition-duration: 1s; */
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
