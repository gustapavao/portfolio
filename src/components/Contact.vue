<script setup>
function contactMe() {
  window.open('https://wa.me/84999340460', '_blank');
}

</script>

<template>
  <div class="container" id="contact">
    <p>Estou aguardando o seu contato:</p>
    <button @click=contactMe>
      Contate-me
    </button>
  </div>
</template>

<style scoped>
  .container{
    display: flex;
    flex-direction: column;
    height: 20rem;
    align-items: center;
    justify-content: center;
    background-color: #0ACF83;
    margin: 5rem 0;
  }
  p {
    text-align: center;
    color: white;
    font-weight: 800;
    font-size: 3rem;
    font-family: Montserrat, sans-serif;
  }
  button {
    width: 30%;
    height: 4rem;
    border-radius: 3rem;
    background-color: var(--color-background);
    font-size: 180%;
    font-weight: 600;
    transition: 0.3s;
    cursor: pointer;
    box-shadow: .6rem .9rem #000;
  }

  button:hover {
    background-color: var(--color-background-prp);
  }

  @media screen and (max-width: 800px) {
    button{
      width: 70%;
    }
  }
</style>