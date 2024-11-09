<script setup>
import icono1 from '/src/assets/ventas.svg';
import icono2 from '/src/assets/ecomerce.svg';


import { ref } from 'vue';
const titulo = 'PMO (Project Management Office)/Práctica de Control de Cálidad (Curso de QA Manual) ';
const fecha = '2018 a 2023';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'Trabaje como PMO (Project Management Office) en la Empresa PGA Group unas de mis principales funciones fueron: Monitoreo y Control: Realizando un seguimiento continuo del progreso de los proyectos, asegurando que se cumplan los plazos, presupuestos y entregables. Incluyendo la identificación y mitigación de riesgos. Informe y Comunicación: Preparando y distribuyendo informes sobre el estado de los proyectos a las partes interesadas. Esto incluía la comunicación de los avances, problemas y cambios en el alcance del proyecto.'  },
    { id: 2, src: icono2, parrafo:  'Serie de técnicas desarrolladas pertinentes a las Pruebas Funcionales. Análisis y Diseño de Casos de Pruebas del sitio web de E-Commerce Demo Blaze .' },
  
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ "Experiencia Profesional".toLocaleUpperCase() }}</h3>
        <p class="fecha"> 2018 a  2023</p>
        <ul class="listado">
            <!-- Experiencia en PGA Group -->
            <li class="item">
                <img class="imagen-svg" src="/src/assets/pmo.svg" width="45rem" alt="PMO en PGA Group">
                <p>Trabajé como PMO (Project Management Office) en PGA Group. Mis principales funciones incluían:</p>
                <ul>
                    <li><strong>Monitoreo y Control:</strong> Realizaba un seguimiento continuo del progreso de los proyectos, asegurando que se cumplieran plazos, presupuestos y entregables. Esto incluía la identificación y mitigación de riesgos.</li>
                    <li><strong>Informe y Comunicación:</strong> Preparaba y distribuía informes sobre el estado de los proyectos a las partes interesadas, comunicando avances, problemas y cambios en el alcance.</li>
                </ul>
            </li>

            <!-- Curso de QA Manual -->
            <li class="item">
                <img class="imagen-svg" src="/src/assets/qa_manual.svg" width="45rem" alt="Curso de QA Manual">
                <p>Práctica de Control de Calidad (Curso de QA Manual): Serie de técnicas desarrolladas pertinentes a las pruebas funcionales.</p>
            </li>

            <!-- Análisis y Diseño de Casos de Pruebas -->
            <li class="item">
                <img class="imagen-svg" src="/src/assets/analisis_diseno.svg" width="45rem" alt="Análisis y Diseño de Casos de Pruebas">
                <p>Análisis y Diseño de Casos de Pruebas: Análisis y diseño de casos de pruebas del sitio web de E-Commerce Demo Blaze.</p>
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