<template>
  <section id="home" class="scene">
    <div class="home-banner fx-row fx-column-responsive fx-align-items-center fx">
      <div class="home-descripcion">
        <h1>Vue</h1>
        <h3>Introducción</h3>
        <p>Vue (pronunciado /vjuː/, como view) es un framework progresivo para construir interfaces de usuario. A
          diferencia de otros frameworks monolíticos, Vue está diseñado desde cero para ser utilizado incrementalmente.
        </p>
      </div>
      <img v-bind:src="image" v-bind:alt="text" class="pfp">
      <img src="../assets/grass.png" class="forest">
    </div>
  </section>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      image: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/250px-Vue.js_Logo_2.svg.png",
      text: "Vue"
    }
  }
}
</script>

<style>
#home {
  height: 100vh;
  background-size: cover;
  color: var(--color-font);
}

.home-banner {
  opacity: 0.9;
  padding: 7rem 10rem;
  z-index: 1;
}

.home-banner>h1 {
  text-transform: uppercase;
  font-size: 2rem;
  width: 100px;
  height: 100px;
}

.home-banner>h3 {
  font-size: 1.5rem;
}

.home-banner>p {
  width: 5rem;
}

.home-descripcion {
  margin-bottom: 5rem;
  margin-right: 5rem;
  padding: 1rem;
  background-color: var(--color-container);
}

.scene {
  position: relative;
  width: 100%;
  height: 100vh;
  background: linear-gradient(#111425, #3751e0);
  background-attachment: fixed;
  overflow: hidden;
}

.forest {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  transform: scale(1.2);
}

.pfp {
  position: relative;
  width: 30%;
  z-index: 1;
}
</style>