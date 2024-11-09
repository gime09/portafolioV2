<script setup>
import { ref } from 'vue';
import FondoLava from './FondoLava.vue';
//Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses
const intereses = ref([
    'Historia y Civilizaciones Antiguas: Me fascina aprender sobre diferentes culturas y civilizaciones a lo largo de la historia, como el Antiguo Egipto y la Grecia clásica.',
    'Lectura de Novelas Clásicas: Disfruto de la literatura clásica y contemporánea, desde obras de Jane Austen hasta autores modernos, lo que me permite explorar nuevas perspectivas.',
    'Pintura y Arte Visual: Practico la pintura en mi tiempo libre, lo que me permite expresar mi creatividad y desconectar de la rutina diaria.',
    'Cine y Crítica Cinematográfica: Me apasiona ver películas de diferentes géneros y épocas, además de analizar sus aspectos artísticos y narrativos.',
    'Estudio de Filosofía: Me interesa leer sobre filosofía y reflexionar sobre los grandes temas de la vida, como el propósito y la ética.',
    'Escritura Creativa: Me gusta escribir relatos cortos y ensayos, lo cual es una excelente forma de desarrollar mi creatividad y mis habilidades comunicativas.',
    'Exploración de Museos y Exposiciones: Visito museos y exposiciones de arte e historia para conocer más sobre diferentes épocas y movimientos artísticos.',
    'Documentales de Historia y Ciencia: Disfruto ver documentales sobre temas históricos y científicos para ampliar mis conocimientos y comprender mejor el mundo.'
]);
</script>

<template>
    <div class="intereses-contenedor">
        <FondoLava />
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
    <!-- <div class="intereses-contenedor">
        <ul class="contenedor-lista">
            <li class="item">
                Desarrollo de Software de Código Abierto: Contribuyo a proyectos en GitHub, colaborando con otros
                desarrolladores para mejorar herramientas y librerías populares.
            </li>
            <li class="item">
                Deportes al Aire Libre: Disfruto del senderismo y el ciclismo de montaña, actividades que practico
                regularmente para mantener un equilibrio entre el trabajo y la vida personal.
            </li>
            <li class="item">
                Tecnología de Innovación: Me apasiona explorar nuevas tendencias tecnológicas como la inteligencia
                artificial y el desarrollo de aplicaciones móviles.
            </li>
            <li class="item">
                Fotografía: Practico la fotografía como un hobby, lo que me ayuda a mantener una perspectiva creativa
                tanto en mi vida profesional como personal.
            </li>
        </ul>
    </div> -->
</template>

<style scoped>
.intereses-contenedor {
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item {
    margin-bottom: 1rem;
}
</style>