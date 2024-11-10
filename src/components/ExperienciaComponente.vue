<script setup>
import icono1 from '/src/assets/ventas.svg';
import icono2 from '/src/assets/ecomerce.svg';


import { ref } from 'vue';
const titulo = 'PMO (Project Management Office)/Práctica de Control de Cálidad (Curso de QA Manual)';
const fecha = '2018 a 2023';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'Trabaje como PMO (Project Management Office) en la Empresa PGA Group unas de mis principales funciones fueron: Monitoreo y Control: Realizando un seguimiento continuo del progreso de los proyectos, asegurando que se cumplan los plazos, presupuestos y entregables. Incluyendo la identificación y mitigación de riesgos. Informe y Comunicación: Preparando y distribuyendo informes sobre el estado de los proyectos a las partes interesadas. Esto incluía la comunicación de los avances, problemas y cambios en el alcance del proyecto.'  },
    { id: 2, src: icono2, parrafo:  'Serie de técnicas desarrolladas pertinentes a las Pruebas Funcionales. Análisis y Diseño de Casos de Pruebas del sitio web de E-Commerce Demo Blaze .' },
  
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{titulo }}</h3>
        <p class="fecha"> {{ fecha }}</p>
        <ul class="listado">
            <!-- Experiencia en PGA Group -->
            <li class="item"  v-for="experiencia in experiencias" :key="experiencia.id">
                <img class="imagen-svg" :src="experiencia.src" width="45rem" :alt="experiencia.parrafo">
                <p>{{ experiencia.parrafo }}</p>
                
            </li> 
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: coral;
}

.fecha {
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>