<script setup>
function contactMe() {
  window.open('https://wa.me/5584999340460', '_blank');
}
</script>

<template>
  <div class="hello-container">
  <div class="hello">
    <p>
      Olá,<br><span class="introduce">Eu sou Gustavo Pavão</span>
    </p>
    <p>
      Full Stack Developer
    </p>
    <div id="button-container">
      <button @click=contactMe >Contrate-me</button>
      <div class="shadow"></div>
    </div>
  </div>
  <div>
    <img id="caric" src="/static/img/CYFzUEcVT72rtblFAin2Mg.png">
  </div>
  </div>

</template>

<style scoped>

  .hello-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
  }
  .hello {
    display: flex;
    flex-direction: column;
    font-size: 4rem;
    font-family: Montserrat;
    font-weight: 800;
  }

  .hello p:last-of-type {
    font-size: 1.5rem;
    color: #474A57;
    font-weight: 600;
    margin-top: -4rem;
  }

  #button-container {
    position: relative;
    display: inline-block;
  }

  button {
    width: 11rem;
    height: 3rem;
    border-radius: 0.8rem;
    border: none;
    background-color: #000;
    color: #fff;
    font-weight: 700;
    font-size: 1.54rem;
    z-index: 1;
    cursor: pointer;
    position: relative;
    transition: all 0.4s ease-in-out;
  }

  button:hover {
    background-color: #FFF;
    color: #000;
  }

  .shadow {
    position: absolute;
    background-color: var(--color-background-mute);
    height: 3rem;
    width: 11rem;
    border-radius: 0.8rem;
    z-index: -1;
    transform: translateY(-3.4rem);
    left: 0.3rem;
  }

  #caric {
    margin-top: 2rem;
    margin-left: 10rem;
    width: 40rem;
    border-radius: 50%;
    background-color: var(--color-background-mute);
    margin-bottom: 5rem;
  }

  @media (max-width: 1600px) {
    #caric {
      width: 20rem;
      margin-left: 15rem;
    }
    .hello {
      display: flex;
      flex-direction: column;
      font-size: 4rem;
      font-family: Montserrat, sans-serif;
      font-weight: 800;
    }
    .introduce {
      font-size: 2rem;
    }
  }

  @media (max-width: 1000px) {
    #caric {
      width: 20rem;
      margin-left: 4rem;
    }
    .hello {
      display: flex;
      flex-direction: column;
      font-size: 3rem;
      font-family: Montserrat, sans-serif;
      font-weight: 800;
    }
    .introduce {
      font-size: 2rem;
    }
  }

</style>