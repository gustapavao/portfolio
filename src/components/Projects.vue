<script setup>
const props = defineProps({
  name: String,
  description: String,
  repository: String,
  link: String,
  tech: Array
})

</script>

<template>
  <div class="project">
    <h2 id="title">{{props.name}}</h2>
    <p id="description">
      {{props.description}}
    </p>
    <div class="technologies">
      <img :src="img" v-for="img in props.tech" alt="">
    </div>
    <a target="_blank" :href=props.repository ><button>Repositório</button></a>
    <a v-if="props.link" :href="props.link" target="_blank">
      <button><img src="" alt="">Aplicação</button>
    </a>
  </div>
</template>

<style scoped>
.project {
  box-sizing: border-box;
  border-radius: 1rem;
  background-color: var(--color-background-prp);
  display: flex;
  flex-direction: column;
  padding: 2rem 4rem;
  box-shadow: 1rem 1rem 1rem #000;
  color: #FFF;
  margin: 2rem 4rem;
  width: 25%;
  height: 40rem;
}

h2 {
  text-align: center;
  font-family: Montserrat, sans-serif;
  font-weight: 800;
  font-size: 3rem;
  overflow-block: clip;
}

p {
  font-family: Montserrat, sans-serif;
  font-weight: 600;
  font-size: 1.1rem;
  margin: 0 0 2rem 0;
}

#description {
  width: 100%;
  height: 30%;
}

.technologies {
  display: flex;
  flex-direction: row;
  height: 10%;
  width: 100%;
  justify-content: center;
  margin-bottom: .9rem;
}

button{
  border: none;
  background-color: var(--color-background);
  margin: .5rem 0 .5rem 0;
  padding: .8rem 2rem;
  border-radius: 0.4rem;
  text-decoration: none;
  font-size: 1.2rem;
  font-weight: bold;
  width: 100%;
}

button:hover {
  background-color: #0ACF83;
  color: #fff;
}

@media (max-width: 1400px) {
  .project {
    width: 45%;
    height: 50rem;
    gap: 2rem;
  }
}

@media (max-width: 1000px) {
  .project{
    box-sizing: inherit;
  }
  .technologies{
    height: 7%;
  }
}

@media (max-width: 800px) {
  .project{
    height: 40rem;
  }
  h2{
    font-size: 1.8rem;
  }
  p{
    font-size: 1rem;
    text-align: center;
  }
}
</style>