<script setup>
import Projects from "@/components/Projects.vue";

// Falta linkar à API e remover esses dados brutos daqui.
const pomonic = {
  name: "Pomonic",
  description: "Pomonic ajuda você a atingir suas metas sem estresse. Mantendo um equilíbrio saudável entre foco e descanso. Foi construido utilizando:",
  tech: ['static/img/tech/vue-svgrepo-com.svg', 'static/img/tech/css-3-svgrepo-com.svg', 'static/img/tech/html-5-svgrepo-com.svg', 'static/img/tech/javascript-svgrepo-com.svg'],
  repository: "https://github.com/gustapavao/pomonic-vue",
  link: "https://pomonic-vue.vercel.app/"
}

// const randoMovie = {
//   name: "RandoMovie",
//   description: "Melhor amigo dos indecisos na hora de escolher um filme. Foi construido utilizando:",
//   tech: ['static/img/tech/vue-svgrepo-com.svg',
//     'static/img/tech/css-3-svgrepo-com.svg',
//     'static/img/tech/html-5-svgrepo-com.svg',
//     'static/img/tech/javascript-svgrepo-com.svg',
//     'static/img/tech/python-svgrepo-com.svg',],
//   repository: "https://github.com/gustapavao/randomovie",
//   link: "https://pavao.life/randomovie",
// }

const portfolio = {
  name: "Portfólio",
  description: "Este portfólio que está olhando agora. Bem construido e melhorando aos poucos.",
  tech: [
    'static/img/tech/vue-svgrepo-com.svg',
    'static/img/tech/css-3-svgrepo-com.svg',
    'static/img/tech/html-5-svgrepo-com.svg',
    'static/img/tech/javascript-svgrepo-com.svg',
  ],
  repository: "https://github.com/gustapavao/portfolio",
  link: "https://portfolio-gustavo-pavaos-projects.vercel.app/"
}

// const projects = {
//   name: "Gestor de Projetos",
//   description: "API que fornece os dados dos meus projetos pessoais, tais como nome, descrição, repositório etc",
//   tech: [
//     'static/img/tech/java-svgrepo-com.svg',
//     'static/img/tech/spring.svg',
//   ],
//   repository: "https://github.com/gustapavao/personal_projects",
//   link: null
// }

const github_findit = {
  name: "GitHub Find it",
  description: "Ferramenta que busca repositórios recentes do usuário buscado e mostra o gráfico das linguagens mais usadas",
  tech: [
    'static/img/tech/atom.png',
    'static/img/tech/css-3-svgrepo-com.svg',
    'static/img/tech/typescript.png',
    'static/img/tech/javascript-svgrepo-com.svg',
    'static/img/tech/tailwind-css-icon-1725660884.png',
  ],
  repository: "https://github.com/gustapavao/github_find_it",
  link: "https://github-find-it.vercel.app/"
}

const barbearia = {
  name: "Barbearia Machado",
  description: "Site feito para a barbearia Machado localizada na minha cidade natal. Pretendo fazer um sistema de agendamento de horários",
  tech: [
    'static/img/tech/atom.png',
    'static/img/tech/css-3-svgrepo-com.svg',
    'static/img/tech/typescript.png',
    'static/img/tech/javascript-svgrepo-com.svg',
    'static/img/tech/tailwind-css-icon-1725660884.png',
  ],
  repository: "https://github.com/gustapavao/barbearia_machado",
  link: "https://barbearia-machado-five.vercel.app/"
}

</script>

<template>
<div class="projects-container" id="projects">
  <div class="projects-header">
    <h1>Projetos</h1>
    <p>
      Alguns projetos que já desenvolvi estão aqui, assim como as tecnologias que usei para desenvolve-los.
    </p>
  </div>
  <div class="projects">
    <Projects :name=pomonic.name :description=pomonic.description :tech=pomonic.tech :repository=pomonic.repository :link=pomonic.link />
<!--    <Projects :name=randoMovie.name :description=randoMovie.description :tech=randoMovie.tech :repository=randoMovie.repository :link=randoMovie.link />-->
    <Projects :name=portfolio.name :description=portfolio.description :tech=portfolio.tech :repository=portfolio.repository :link=portfolio.link />
<!--    <Projects :name=projects.name :description=projects.description :tech=projects.tech :repository=projects.repository :link=projects.link />-->
    <Projects :name=github_findit.name :description=github_findit.description :tech=github_findit.tech :repository=github_findit.repository :link=github_findit.link />
    <Projects :name=barbearia.name :description=barbearia.description :tech=barbearia.tech :repository=barbearia.repository :link=barbearia.link />
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