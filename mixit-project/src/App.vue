<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HelloWorld from './components/Landing.vue'
import Landing from './components/Landing.vue';
import Header from "./components/Header.vue"
import Footer from "./components/Footer.vue"
import Offer from './components/landing/Offer.vue'
import Novedades from './components/landing/Novedades.vue'
</script>


<template>
<div>
    <header>
    <Header></Header>
  </header>
  <div>
    <Landing></Landing>
  </div>

  <div class="components">
    <div class="component">
      <div class="squard">
        <img src="./assets/leaf.png" alt="">
      </div>
      <p>No contiene SLS</p>
    </div>

    <div class="component">
      <div class="squard">
        <img src="./assets/tree.png" alt="">
      </div>
      <p>No contiene paarabenos</p>
    </div>

    <div class="component">
      <div class="squard">
        <img src="./assets/diamond.png" alt="">
      </div>
      <p>No contiene aceites minerales</p>
    </div>

    <div class="component">
      <div class="squard">
        <img src="./assets/rabbit.png" alt="">
      </div>
      <p>No testeado en animales</p>
    </div>

    <div class="component">
      <div class="squard">
        <img src="./assets/leafatom.png" alt="">
      </div>
      <p>Desarrollado con tecnologias actuales</p>
    </div>

    <div class="component">
      <div class="squard">
        <img src="./assets/hands.png" alt="">
      </div>
      <p>Programa de cuidad de la piel de 4 pasos</p>
    </div>

    <div class="component">
      <div class="squard">
        <img src="./assets/girl.png" alt="">
      </div>
      <p>Para cualquier tipo de piel</p>
    </div>

    <div class="component">
      <div class="squard">
        <img src="./assets/quimica.png" alt="">
      </div>
      <p>Probado clinicamente</p>
    </div>
  </div>

  <div>
    <p id="novedades">Nuestros novedades</p>
    <Novedades></Novedades>
  </div>

  <div class="informe">
    <p>Informate sobre nuestros nuevas colecciones</p>
    <input type="text" placeholder="EMAIL">
    <button>Seguir</button>
  </div>

  <footer>
    <Footer></Footer>
  </footer>
</div>

</template>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.components{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 10px 20px 10px 20px;
}

.component{
  /* border: 2px firebrick solid; */
  width: 12.5%;
  align-items: center;
  display: flex;
  flex-direction: column;
  padding: 0 4px;
}

.squard{
  border: 2px #eb83ae solid;
  height: 80px;
  width: 80px;
  border-radius: 50%;
  align-self: center;
  /* align-items: center; */
  justify-content: center;
  display: flex;
}

.squard img{
  width: 90%;
  height: 90%;
  border-radius: 50%;
  align-self: center;
  align-items: center;
}

.informe{
  font-size: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 30px;
  margin-top: 30px;
}

.informe input{
  height: 30px;
  width: 250px;
  border-radius: 10px;
  border: 1px rgba(0, 0, 0, 0.445) solid;
  color: black;
  padding-left: 20px;
}

.informe input::placeholder{
  text-align: center;
  padding-right: 10px;
}

.informe button{
  border: none;
  height: 40px;
  width: 150px;
  border-radius: 50px;
  background-color: #eaba0a;
  color: white;
  font-size: 20px;
  margin-top: 20px;
}

#novedades{
  font-size: 25px;
}
</style>
