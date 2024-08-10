<script setup>
import Projects from "@/components/Projects.vue";

const pomonic = {
  name: "Pomonic",
  description: "Um pomodoro que ajuda no foco ao realizar tarefas diárias. Foi construido utilizando:",
  tech: ['static/img/tech/vue-svgrepo-com.svg', 'static/img/tech/css-3-svgrepo-com.svg', 'static/img/tech/html-5-svgrepo-com.svg', 'static/img/tech/javascript-svgrepo-com.svg'],
  repository: "https://github.com/gustapavao/pomonic",
  link: "https://pavao.life/pomonic"
}

const randoMovie = {
  name: "RandoMovie",
  description: "Uma aplicação para selecionar filmes a partir de uma watchlist do letterboxd ou receber um filme aleatório. Foi construido utilizando:",
  tech: ['static/img/tech/vue-svgrepo-com.svg',
    'static/img/tech/css-3-svgrepo-com.svg',
    'static/img/tech/html-5-svgrepo-com.svg',
    'static/img/tech/javascript-svgrepo-com.svg',
    'static/img/tech/java-svgrepo-com.svg',
    'static/img/tech/python-svgrepo-com.svg',],
  repository: "https://github.com/gustapavao/randomovie",
  link: "https://pavao.life/randomovie",
}
</script>

<template>
<div class="projects-container" id="projects">
  <div class="projects-header">
    <h1>Projects</h1>
    <p>
      Alguns projetos que já desenvolvi estão aqui, assim como as tecnologias que usei para desenvolve-los.
    </p>
  </div>
  <div class="projects">
    <Projects :name=pomonic.name :description=pomonic.description :tech=pomonic.tech :repository=pomonic.repository :link=pomonic.link />
    <Projects :name=randoMovie.name :description=randoMovie.description :tech=randoMovie.tech :repository=randoMovie.repository :link=randoMovie.link />
  </div>
</div>
</template>

<style scoped>
.projects-container {
  margin-top: 5rem;
  padding-top: 4rem;
  padding-bottom: 4rem;
  width: 100%;
  flex-wrap: wrap;
  background-color: var(--color-background-oran);
}

.projects-header {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 15rem;
}

h1 {
  font-family: Montserrat,sans-serif;
  font-size: 5rem;
  font-weight: 800;
  margin: auto;
  color: #000;
}

p {
  font-family: Montserrat,sans-serif;
  font-size: 1.5rem;
  text-align: center;
  font-weight: 600;
  color: #ffffff;
  margin-top: -3rem;
}

.projects {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
}

@media (max-width: 1400px) {
  h1 {
    font-size: 2.5rem;
  }
  p {
    font-size: 1rem;
    padding: .5rem;
  }
  .projects {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
  }

}

@media (max-width: 1000px) {
  .projects {
    margin-left: -1rem;
  }
}
</style>