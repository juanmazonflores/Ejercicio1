<template>
  <section id="acerca">
    <h1>¿Que es Vue?</h1>

    <div class="acerca-container fx-row fx-column-responsive fx-content-space-between fx-align-items-center">

      <div class="acerca-info fx-column">
        <div class="acerca-contenido fx-row">
          <div class="acerca-icono">
            <img src="../assets/info.png" alt="Info">
          </div>
          <div class="acerca-texto">
            <h3>Introducción</h3>
            <div class="acerca-item">
              <h4>// ¿Para que es?:</h4>
              <p>* La librería central está enfocada solo en la capa de visualización, y es fácil de utilizar e integrar
                con otras librerías o proyectos existentes.</p>
              <p>* Por otro lado, Vue también es perfectamente capaz de impulsar sofisticadas Single-Page Applications
                cuando se utiliza en combinación con herramientas modernas y librerías de apoyo.</p>
            </div>
            <button v-if="!mostrar" @click="Mostrar" class="button-action">Ver Mas</button>
            <button v-if="mostrar" @click="Mostrar" class="button-action">Ver Menos</button>
            <div v-if="mostrar" class="acerca-item">
              <h4>// ¿Como probarlo?</h4>
              <p>* La forma más fácil de probar Vue.js es usando el ejemplo Hola Mundo en JSFiddle. Siéntase libre de
                abrirlo en otra pestaña y seguirlo mientras analizamos algunos ejemplos básicos. O puede crear un archivo
                index.html e incluir Vue con:</p>
            </div>

          </div>
        </div>
      </div>


      <div class="acerca-video fx-column fx-align-items-center fx-content-center">
        <h3>Un poco más de Vue.js</h3>
        <iframe src="https://drive.google.com/file/d/1zJ-V0bUuU_IaasNSH_sNbTN3p3D4hzwH/preview" width="640" height="480"
          allow="autoplay"></iframe>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
let mostrar = ref(false);
const Mostrar = () => {
  if (mostrar.value) {
    mostrar.value = false;
  } else {
    mostrar.value = true;
  }

};
</script>

<script>

export default {
  name: 'Intro',
}

</script>

<style>
.acerca-container {
  padding: 0 90px;
  gap: 90px;
}

.acerca-video {
  flex: 1;
  text-align: center;
  padding: 2rem;
  color: var(--color-font);
  background: var(--color-container);
  box-shadow: 0 10px 8px rgba(95, 186, 167, 0.1);
}

.acerca-video iframe {
  width: auto;
  margin-top: 1rem;
}

.acerca-video h3,
.acerca-video p {
  margin-top: 1rem;
}


.acerca {
  flex: 1;
  gap: 20px;
}

.acerca-item {
  margin-top: 1.5rem;
}

.acerca-contenido {
  gap: 10px;
  padding: 15px;
}

.acerca-icono img {
  width: 40px;
  border-radius: 50%;
}

.acerca-texto {
  flex: 1;
  color: var(--color-font2);
  line-height: 150%;

}
</style>