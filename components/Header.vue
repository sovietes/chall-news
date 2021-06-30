<template>
  <header>
    <section class="container">
      <div class="info">
        <p>Codelândia</p>
        <p>blog</p>
      </div>
      <form class="input-search">
        <input
          v-model="contentText"
          type="text"
          class="search"
          placeholder="Pesquisar no blog"
        />
        <img src="@/assets/img/Vector.svg" alt="Pesquisar vetor" />
        <ion-icon
          v-show="haveContent"
          name="close-outline"
          @click="clear"
        ></ion-icon>
      </form>
    </section>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      contentText: '',
      haveContent: false,
    }
  },

  watch: {
    contentText(value) {
      if (value.length > 0) {
        this.haveContent = true
      } else {
        this.haveContent = false
      }
    },
  },

  methods: {
    clear() {
      this.contentText = ''
    },
  },
})
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
  padding-right: 3.5rem;
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

ion-icon {
  color: white;
  position: absolute;
  font-size: 24px;
  right: 0.7rem;
  top: 50%;
  transform: translateY(-50%);
  padding: 0.3rem;
  background: rgba(128, 128, 128, 0.432);
  border-radius: 5px;
  cursor: pointer;
}
</style>
