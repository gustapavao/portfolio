<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
  }
</script>

<template>
  <header class="header">
    <div class="logo-container">
      <img src="/static/img/g.png" alt="letter g" style="max-width: 4rem">
    </div>
    <div class="navigation">
      <nav>
        <ul :class="{'nav-list': true, 'active': isMenuOpen}">
          <li><a href="">Inicio</a></li>
          <li><a href="">Sobre</a></li>
          <li><a href="">Contato</a></li>
          <li><a href="">Projetos</a></li>
        </ul>
        <button @click="toggleMenu" class="menu-toggle" aria-label="Toggle menu">
          <span class="menu-icon"></span>
        </button>
      </nav>
    </div>
  </header>
</template>

<style scoped>
  header {
    display: flex;
    width: 100%;
    justify-content: space-around;
    align-items: center;
    background-color: #000;
    border-bottom-left-radius: 3rem;
    border-bottom-right-radius: 3rem;
  }

  .logo-container{
    display: flex;
    align-items: center;
  }

  .navigation{
    display: flex;
    align-items: center;
  }

  .nav-list {
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .nav-list li {
    margin: 0 1rem;
  }

  .nav-list a {
    text-decoration: none;
    color: #FFF;
    font-size: 2rem;
    font-weight: bold;
  }

  .menu-toggle {
    display: none;
    background: none;
    border: none;
    cursor: pointer;
    font-size: 2rem;
    color: #FFF;
  }

  .menu-icon::before {
    content: "☰";
  }

  @media (max-width: 768px) {
    .header {
      justify-content: center;
      position: relative;
      border-radius: 0;
    }

    .logo-container {
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
    }

    .navigation {
      width: 100%;
      flex-direction: column;
      align-items: flex-start;

    }

    .nav-list {
      display: none;
      flex-direction: column;
      width: 100%;
    }

    .nav-list.active {
      display: flex;
    }

    .nav-list li {
      margin: 1rem 0;
    }

    .menu-toggle {
      display: block;
    }
  }
</style>