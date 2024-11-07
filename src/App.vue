<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import Educacion from './components/EducacionComponente.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue'
import HabilidadesComponente from './components/HabilidadesComponente.vue';
</script>

<template>
    <header id="top">
        <!-- Barra de navegacion -->
        <NavBar />
        <!-- Componente Datos Personales-->
        <DatosPersonales />
    </header>
    <main>
        <!-- el estilo css de section se encuentra en base css-->
        <section id="educacion"><h2>Educación - Cursos</h2>
        <Educacion />
        </section>
        <section id="experiencia"><h2>Experiencia</h2>
        <ExperienciaComponente />
      </section>
        <section id="habilidades"><h2>Habilidades</h2>
        <HabilidadesComponente />
      </section>
    </main>
    <footer>
      <a href="#top">Inicio</a>
      <p>© 2024 Luciana Fragueiro - Portafolio web</p>
    </footer>
</template>

<style scoped>
footer{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  font-size: 1.3rem;
}
</style>

