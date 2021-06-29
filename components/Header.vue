<template>
  <header>
    <section class="container">
      <div class="info">
        <p>Codelândia</p>
        <p>blog</p>
      </div>
      <form class="input-search">
        <input type="text" class="search" placeholder="Pesquisar no blog" />
        <img src="@/assets/img/Vector.svg" alt="Pesquisar vetor" />
      </form>
    </section>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style scoped>
header {
  background: linear-gradient(90deg, #574ae8 0%, #3ea1db 100%);
}

.container {
  max-width: 1100px;
  width: 100%;
  margin: 0 auto;
  height: 15.625rem;
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-direction: column;
  width: 100vw;
  padding: 0 2rem;
}

.search {
  width: 100%;
  height: 100%;
  border-radius: 5px;
  border: none;
  padding-left: 3.5rem;
  padding-right: 0.5rem;
  font-size: 1.125rem;
  background: rgba(255, 255, 255, 0.2);
  font-family: 'Inter', sans-serif;
  font-style: normal;
}

input::placeholder {
  color: #ffffff;
  opacity: 0.5;
}

.input-search {
  width: 100%;
  height: 4.0625rem;
  position: relative;
}

img {
  position: absolute;
  left: 1rem;
  top: 50%;
  transform: translateY(-50%);
}

p {
  font-family: 'Lexend Deca';
  font-size: 1.5rem;
}

.info {
  display: flex;
  justify-content: space-between;
  width: 100%;
}
</style>
