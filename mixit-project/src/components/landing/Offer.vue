<script setup>
import { ref } from 'vue'

var producto = [
    {
        fotourl : "../../assets/product1.png",
        descr : 'Sunscreen lotion para el cuerpo con purpurina, SPF30, 50ml',
        stars: 3,
        precio: 5.9
    },
    {
        fotourl : "@/../product2.png",
        descr : 'Sunscreen lotion para el cuerpo con purpurina, SPF20, 100ml',
        stars: 3,
        precio: 5.9 
    },
        {
        fotourl : "product3.png",
        descr : 'Sunscreen spray-mist para el cuerpo, SPF20, 150ml',
        stars: 3,
        precio: 5.0 
    },
    {
        fotourl : "product4.png",
        descr : 'Aceite-bronceador con extracto de bayas godji',
        stars: 3,
        precio: 5.9 
    }
]

function favorite(index){
    console.log("Hola")
    let h = document.getElementById("heart")
    let hf = document.getElementById("heart-fill")

    if(h.style.visibility == "hidden"){
        h.style.visibility = "visible"
        hf.style.visibility = "hidden"
    }
    else{
        hf.style.visibility = "visible"
        h.style.visibility = "hidden"
    }
}

defineProps({
  msg: String
})

const count = ref(0)
</script>


<template>

<div class="contenedor-producto">
    <div v-for="(object, index) in producto" :key="index"  class="cont-offer">

        <div class="personal">
            <img src="" alt="new">
            <!-- <img src="../../../assets/logo.png'" alt="heart"> -->
            <div @click="favorite(index)" class="hearts" :id="index">
                <svg id="heart" xmlns="http://www.w3.org/2000/svg" width="27" height="27" fill="currentColor" class="bi bi-heart" viewBox="0 0 16 16">
                    <path d="m8 2.748-.717-.737C5.6.281 2.514.878 1.4 3.053c-.523 1.023-.641 2.5.314 4.385.92 1.815 2.834 3.989 6.286 6.357 3.452-2.368 5.365-4.542 6.286-6.357.955-1.886.838-3.362.314-4.385C13.486.878 10.4.28 8.717 2.01L8 2.748zM8 15C-7.333 4.868 3.279-3.04 7.824 1.143c.06.055.119.112.176.171a3.12 3.12 0 0 1 .176-.17C12.72-3.042 23.333 4.867 8 15z"/>
                </svg>
                <svg id="heart-fill" xmlns="http://www.w3.org/2000/svg" width="27" height="27" fill="currentColor" class="bi bi-heart-fill" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M8 1.314C12.438-3.248 23.534 4.735 8 15-7.534 4.736 3.562-3.248 8 1.314z"/>
                </svg>
            </div>

        </div>
        <div class="foto"> 
            <img :src="object.fotourl" alt="producto">
            
        </div>
        <div class="descr-precio">
            <p id="decription">{{object.descr}}</p>
            <p>{{object.precio}} € </p>

        </div>
        <button> <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-cart-plus" viewBox="0 0 16 16">
            <path d="M9 5.5a.5.5 0 0 0-1 0V7H6.5a.5.5 0 0 0 0 1H8v1.5a.5.5 0 0 0 1 0V8h1.5a.5.5 0 0 0 0-1H9V5.5z"/>
            <path d="M.5 1a.5.5 0 0 0 0 1h1.11l.401 1.607 1.498 7.985A.5.5 0 0 0 4 12h1a2 2 0 1 0 0 4 2 2 0 0 0 0-4h7a2 2 0 1 0 0 4 2 2 0 0 0 0-4h1a.5.5 0 0 0 .491-.408l1.5-8A.5.5 0 0 0 14.5 3H2.89l-.405-1.621A.5.5 0 0 0 2 1H.5zm3.915 10L3.102 4h10.796l-1.313 7h-8.17zM6 14a1 1 0 1 1-2 0 1 1 0 0 1 2 0zm7 0a1 1 0 1 1-2 0 1 1 0 0 1 2 0z"/>
            </svg>
        </button>

    </div>

</div>
    
</template>

<style>
.contenedor-producto{
    /* border: 2px goldenrod solid; */
    width: 100%;
    margin: 0 15px;
    height: 330px;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

.cont-offer{
    width: 200px;
    border: 2px goldenrod solid;
    height: 100%;
}

.hearts{
    display: flex;
}

#heart{
    transition: all 0.5s ease-out;
}

#heart-fill{
    position: absolute;
    visibility: hidden;
    transition: all 0.5s ease-out;
}

.contenedor-producto button{
    background-color: goldenrod;
    border: none;
    height: 33px;
    width: 60px;
    border-radius: 16px;
    margin-bottom: 10px;
    cursor: pointer;
}

.personal{
    /* border: 2px blue solid; */
    height: 27px;
    display: flex;
    justify-content: space-between;
}

#decription{
    font-size: 13px;
}

.foto{
    height: 150px;
    /* border: 2px hotpink solid; */
    align-self: center;
    align-items: center;
    display: flex;
    justify-content: center;
}

.foto img{
    height: 160px;
    width: 160px;
    display: flex;
}
</style>