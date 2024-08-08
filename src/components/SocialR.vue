<script setup>

</script>

<template>
  <div class="networks">
    <a href="https://github.com/gustapavao"><img src="/static/img/icons8-github.svg"></a>
    <a href="https://www.linkedin.com/in/gustavopavao/"><img src="/static/img/icons8-linkedin.svg"></a>
    <a href="https://www.instagram.com/gustapavao/"><img src="/static/img/icons8-instagram(1).svg"></a>
    <a href="https://x.com/gustavopavao"><img src="/static/img/icons8-twitter.svg"></a>
  </div>
</template>

<style scoped>
.networks {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  height: 8rem;
}

.networks img {
  width: 5rem;
  filter: grayscale(100%) opacity(60%);
  transition: 0.3s ease;
}

.networks img:hover {
  filter: grayscale(0%) opacity(100%);
}

</style>