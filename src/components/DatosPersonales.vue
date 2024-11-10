<script setup>
import linkedin from '/src/assets/icons/linkedin-rounded-border.svg';
import instagram from '/src/assets/instagram_icon.svg';
import github from '/src/assets/github_icon.svg';
import cv from '/src/assets/cv_resume_icon.svg';

const title = 'Gimena Gauna';
const descripcion = 'Estudiante: Técnico Universitario en Programación - UTN';
const residencia = 'Mendoza, Argentina';
const presentacion = '¡Bienvenidos a mi portafolio! Soy Gimena Gauna, Profesora de Historia de formación, pero mi trayectoria me llevó al mundo digital. Mi interés inicial se centró en el Marketing Digital, donde obtuve una diplomatura y realicé varios cursos. Más tarde, mi enfoque cambió hacia el ámbito de la Tecnología de la Información, incursionando en áreas como Full Stack, Gestión de Proyectos Informáticos y Testing QA ⚙️🔎. Fue precisamente este último campo el que me atrapó por completo; me sentí tan cómoda y apasionada que decidí profundizar y profesionalizarme aún más Para mí, la formación continua es fundamental. El mundo tecnológico avanza rápidamente y es crucial mantenerse al día con estos cambios. Mi objetivo principal es sumergirme por completo en el universo ☄️🪐🌕💫  del Testing. Por ello, actualmente me estoy especializando en cursos de Testing Automatizados 🤖, con el fin de alcanzar un dominio total en esta área. ¡El aprendizaje constante es la clave para avanzar al ritmo que demanda la evolución tecnológica! 💻📱✨Actualmente, me encuentro cursando la Tecnicatura de Software en UTN (Facultad Regional San Rafael).👩🏼‍💻'


      
      
const redesSociales = [
  { id: 1, name: 'linkedin', src: linkedin, url: 'https://www.linkedin.com/in/gimena-gauna-08925a197/' },
  { id: 2, name: 'Instagram', src: instagram, url: 'https://www.instagram.com/gimegauna12345678/' },
  { id: 3, name: 'github', src: github, url:  'https://github.com/' },
  { id: 4, name: 'curriculum', src: cv, url: 'https://panoramic-teller-a6b.notion.site/Tester-Manual-Portafolio-b07eb1a4029b46d786dfb2950e5cf386?pvs=4' },
];
const telefono = '+54 9 2615259143';
</script>

<template>
  <section class="datos-personales">
    <div class="card">
      <h1>{{ title }}</h1>
      <h2>{{ descripcion }}</h2>
      <p>{{ presentacion }}</p>
      <ul class="container-lista">
        <li v-for="red in redesSociales" :key="red.id">
          <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
        </li>
      </ul>
      <h3>☎ Mi Teléfono personal:{{ telefono }} </h3>
      <h4>{{ residencia }} </h4>
    </div>
  </section>
</template>

<style scoped>
h1 {
  font-size: 2.5rem;
}

p {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.card {
  background-color: rgb(28, 41, 52);
  border-radius: 10px;
  padding: 10px;
  margin: 10px;
  text-align: center;
}

.container-lista {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: center;
}

.icon-redsocial {
  align-items: center;
  background-color: aliceblue;
  border-radius: 50%;
  padding: 2px;
  margin: 5px;
  box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover {
  background-color: rgb(28, 41, 52);
  box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3 {
  font-size: 1.2rem;
  font-weight: 600;
}
</style>
