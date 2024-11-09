<script setup>
import img1 from '/src/components/icons/html-css.svg';
import img2 from '/src/components/icons/sql.svg';
import img3 from '/src/components/icons/java.svg';
import img4 from '/src/components/icons/jira.svg';
import img6 from '/src/components/icons/mantis.svg';
import img7 from '/src/components/icons/soapui.svg';
import img8 from '/src/components/icons/postman.svg';
import img9 from '/src/components/icons/casos_pruebas.svg';
import img10 from '/src/components/icons/pruebas_no_funcionales.svg';
import img11 from '/src/components/icons/gestion_proyectos.svg';
//Se importa ref de vue para poder usarlo
import { ref } from 'vue';
//Se crea un array de objetos con las habilidades
//Este es un array de objetos con habilidades que se pueden modificar o agregar
const habilidades = ref([
    {// Se crea un objeto con id, nombre y habilidades
        id: 1, nombre: 'Pruebas y Testing', habilidades: [
            { id: 1, nombre: 'Casos de Pruebas', nivel: 'Avanzado', icono: img9 },
            { id: 2, nombre: 'Pruebas No Funcionales', nivel: 'Intermedio', icono: img10 },
            { id: 3, nombre: 'Gestión de Pruebas: Jira y TestLink', nivel: 'Avanzado', icono: img4 },
            { id: 4, nombre: 'Gestión de Defectos: Mantis', nivel: 'Intermedio', icono: img6 }
        ]
    },
    {
        id: 2, nombre: 'Desarrollo Web', habilidades: [
        { id: 1, nombre: 'HTML y CSS', nivel: 'Avanzado', icono: img1 },
            { id: 2, nombre: 'Bases de Datos y SQL', nivel: 'Intermedio', icono: img2 },
            { id: 3, nombre: 'Desarrollo Full Stack con Java', nivel: 'Intermedio', icono: img3 }
        ]
    },
    {
        id: 3, nombre: 'Gestión de Proyectos', habilidades: [
            { id: 1, nombre: 'Gestión de Proyectos', nivel: 'Avanzado', icono: img11 }
         
        ]
    },
    {
        id: 4, nombre: 'Bases de Datos', habilidades: [
            
        { id: 1, nombre: 'SOAP UI', nivel: 'Intermedio', icono: img7 },
        { id: 2, nombre: 'Postman', nivel: 'Intermedio', icono: img8 }
            
        ]
    },

]);

</script>


<template>
    <!--Este componente vue funciona de esta forma:-->
    <div class="skills-contenedor"></div>
    <!-- Se recorre el array habilidades con v-for y se asigna la key habilidad.id-->
      <p><strong>Mis habilidades y conocimientos son los siguientes 👇🏼</strong></p>
        <div v-for="habilidad in habilidades" :key="habilidad.id" class="skills-categoria">
            <!-- Se muestra el nombre de la habilidad-->
            <h3>{{ habilidad.nombre }}</h3>
            <ul class="skills">
              <!--    Se recorre el array habilidades con v-for y se asigna la key habilidad.id-->
                <li v-for="habilidad in habilidad.habilidades" :key="habilidad.id" class="skill">
                <!--Se muestra el icono de la habilidad y el nombre de la habilidad con su nivel-->
                  <img :src="habilidad.icono" :alt="habilidad.nombre">
                    <!--Se muestra el icono de la habilidad y el nombre de la habilidad con su nivel-->
                   <span>{{ habilidad.nombre }}: {{ habilidad.nivel }}</span>
               </li>
            </ul>
        </div>
     

 <!--   <div class="skills-contenedor">
    <div class="skills-categoria">
        <h3>Pruebas y Testing</h3>
        <ul class="skills">
            <li class="skill">
                <img src="/src/components/icons/casos_pruebas.svg" alt="Casos de Pruebas">
                <span>Casos de Pruebas: Avanzado</span>
            </li>
            <li class="skill">
                <img src="/src/components/icons/pruebas_no_funcionales.svg" alt="Pruebas No Funcionales">
                <span>Pruebas No Funcionales: Intermedio</span>
            </li>
            <li class="skill">
                <img src="/src/components/icons/jira.svg" alt="Jira">
                <span>Herramienta de Gestión de Pruebas: Jira y TestLink</span>
            </li>
            <li class="skill">
                <img src="/src/components/icons/mantis.svg" alt="Mantis">
                <span>Herramienta de Gestión de Defectos: Mantis</span>
            </li>
        </ul>
    </div>-->

  <!--  <div class="skills-categoria">
        <h3>Desarrollo Web</h3>
        <ul class="skills">
            <li class="skill">
                <img src="/src/components/icons/html-css.svg" alt="HTML y CSS">
                <span>HTML y CSS: Avanzado</span>
            </li>
            <li class="skill">
                <img src="/src/components/icons/sql.svg" alt="SQL">
                <span>Bases de Datos y SQL: Intermedio</span>
            </li>
            <li class="skill">
                <img src="/src/components/icons/java.svg" alt="Java">
                <span>Desarrollo Full Stack con Java: Intermedio</span>
            </li>
        </ul>
    </div>-->

   <!-- <div class="skills-categoria">
        <h3>Gestión de Proyectos</h3>
        <ul class="skills">
            <li class="skill">
                <img src="/src/components/icons/gestion_proyectos.svg" alt="Gestión de Proyectos">
                <span>Gestión de Proyectos: Avanzado</span>
            </li>
        </ul>
    </div>-->

  <!--  <div class="skills-categoria">
        <h3>Servicios Web y Herramientas</h3>
        <ul class="skills">
            <li class="skill">
                <img src="/src/components/icons/soapui.svg" alt="SOAP UI">
                <span>SOAP UI: Intermedio</span>
            </li>
            <li class="skill">
                <img src="/src/components/icons/postman.svg" alt="Postman">
                <span>Postman: Intermedio</span>
            </li>
        </ul>
    </div>
</div> -->

</template>

<style scoped>
.skills-contenedor {
    padding: 2rem;
    /*Fondo cargado desde una imagen estatica en Assets*/
    /* background-image: url('/src/assets/fondo-proyectos.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat; */
    /*Fondo con gradiente*/
    background: linear-gradient(-45deg, #021526, #03346E, #6EACDA, #E2E2B6);
    /*Fondo con color solido*/
    /* background-color: rgb(28, 41, 52); */
}

.skills-categoria {
    margin-bottom: 20px;
}

.skills-categoria h3 {
    display: flex;
    justify-content: left;
    margin-bottom: 10px;
    font-size: 1.5em;
    color: aliceblue;
    font-size: 1.5em;
    font-weight: bold;
}

.skills {
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    gap: 20px;
}

.skill {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    background-color: rgba(241, 245, 243, 0.856);
    padding: 0.3em;
    border-radius: 8px;
    box-shadow: 0px 4px 12px rgba(2, 151, 151, 0.963);
    flex: 1 1 200px;
    max-width: 250px;
}

.skill:hover {
    background-color: rgba(2, 151, 151, 0.963);
}

.skill img {
    width: 35px;
    height: 35px;
}

.skill span {
    font-size: 1em;
    color: #333;
}

.skill:hover {
    font-size: 1.3em;
    transition: 2s ease;
}

@media (max-width: 768px) {
    .skills-categoria h3 {
        justify-content: center;
    }

    .skill {
        justify-content: center;
    }
}
</style>