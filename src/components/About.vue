<script setup>

</script>

<template>
  <div class="about-container" id="about">
    <div class="img-container">
      <img src="/static/img/myself2.png" alt="" id="myself">
      </div>
    <div class="text-container">
      <h2>Sobre mim</h2>
      <h4>Full Stack Developer</h4>
      <p>
        Sou um jovem programador que atualmente está cursando o primeiro semestre do curso de Bacharelado em Tecnologia da Informação (UFRN).
        Apesar de estar no ínicio da graduação, tenho mais de 2 anos de experiência no mundo do desenvolvimento web.
      </p>
    </div>
  </div>
</template>

<style scoped>
div h2, div h4, p {
  margin: 0;
}

.about-container {
  background-color: var(--color-background-secondary);
  max-width: 90%;
  height: 40rem;
  border-radius: 5rem;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  margin: auto;
}

.img-container {
  position: relative;
  background-color: var(--color-background-mute);
  max-width: 22rem;
  border: 0.2rem solid #000;
  box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.3);
  left: -5rem;
  transition: all 0.6s ease;
}

#myself{
  width: 22rem;
  position: inherit;
}

.img-container:hover{
  transform: translateY(-2rem) translateX(-2rem);
  box-shadow: 1rem 1rem #000;
}

.text-container{
  max-width: 50%;
}

.text-container *{
  margin: 1rem 0;
}

div h2 {
  font-family: Montserrat, sans-serif;
  font-weight: 800;
  font-size: 4rem;
  color: #FFF;
  line-height: 2.5rem;
}

div h4 {
  font-family: Montserrat, sans-serif;
  font-weight: 700;
  font-size: 2rem;
  color: #FFDD55;
}

p {
  max-width: 80%;
  color: #FFF;
  font-family: Montserrat, sans-serif;
  font-weight: 700;
  font-size: 1.5rem;
}

@media (max-width: 1400px) {
  .about-container{
    flex-direction: row;
    flex-wrap: wrap;
    height: auto;
    border-radius: 0.8rem;
  }

  .img-container{
    display: none;
  }

  .text-container{
    max-width: 80%;
    padding: 3rem;
  }

  div h2{
    font-size: 3rem;
  }

  div h4{
    font-size: 1.5rem;
  }
  div p{
    max-width: 95%;
    font-size: 1rem;
    text-align: justify;
  }
}
</style>
