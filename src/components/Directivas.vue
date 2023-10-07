<template>
    <section id="directivas">
        <h1>Directivas</h1>
        <div class="directiva-container fx-row fx-content-center">
            <div class="directiva">
                <h3>Directivas Condicionales</h3>
                <div class="directiva-lista fx-column fx-content-center">
                    <div class="directiva-lista fx-row fx-content-center">
                        <ul>
                            <li v-for="(directiva, index) in arrayDirCondicionales" :key="index">
                                <h4>{{ directiva.name }}</h4>
                                <p>{{ directiva.description }}</p>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="directiva">
                <h3>Directivas de Bucle</h3>
                <div class="directiva-lista fx-column fx-content-center">
                    <div class="directiva-lista fx-row fx-content-center">
                        <ul>
                            <li v-for="(directiva, index) in arrayDirBucle" :key="index">
                                <h4>{{ directiva.name }}</h4>
                                <p>{{ directiva.description }}</p>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="directiva">
                <h3>Entornos de Desarrollo</h3>
                <div class="directiva-lista fx-column fx-content-center">
                    <div class="habilidad-lista fx-row fx-content-center">
                        <ul>
                            <li v-for="(directiva, index) in arrayDirEnlace" :key="index">
                                <h4>{{ directiva.name }}</h4>
                                <p>{{ directiva.description }}</p>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>


<script setup>

const arrayDirCondicionales = [
    {
        name: "v-if",
        description: "La directiva v-if se usa para mostrar o ocultar un elemento de la plantilla"
    },
    {
        name: "v-else",
        description: "Un elemento v-else debe seguir inmediatamente a un v-if o un v-else-if elemento; de lo contrario, no se reconocerá"
    },
    {
        name: "v-show",
        description: "La directiva v-show se usa para mostrar o ocultar un elemento de la plantilla",
    },
];
const arrayDirBucle = [
    {
        name: "v-for",
        description: "a directiva v-for se usa para iterar sobre una lista de elementos."
    },
];
const arrayDirEnlace = [
    {
        name: "v-bind",
        description: "Lo bigotes o llaves dobles no se pueden insertar dentro de los atributos HTML. En su lugar utilice una v-bind para enlazar el valor de un atributo."
    },
];



</script>
<script>
export default {
    name: 'Directivas',
}

</script>

<style>
.directiva-container {
    flex-flow: wrap;
}

.directiva {
    position: relative;
    max-width: 350px;
    overflow: hidden;
    padding: 20px;
    margin: 20px;
    background: var(--color-container2);
    box-shadow: 10px 10px rgba(0, 0, 0, 0.1);
    text-align: center;

}

.directiva-lista img {
    margin-left: 1rem;
    margin-bottom: 1rem;
}


.directiva h3 {
    margin-top: 1rem;
    margin-bottom: 1rem;
    font-size: 1.5rem;
}

.directiva p {
    margin-bottom: 1rem;
    margin-top: 0.25rem;
}

.directiva ul{
    list-style: none;
}
</style>