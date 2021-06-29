<template>
  <div class="card">
    <div class="date">
      <p class="date-font">{{ date }}</p>
      <img src="@/assets/img/heart.svg" alt="" />
    </div>
    <div class="title">
      <p class="title-font">{{ title }}</p>
    </div>
    <div class="content">
      <p class="content-font">{{ content }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    date: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    content: {
      type: String,
      required: true,
    },
  },
})
</script>

<style scoped>
/* Gerais */
.card {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-bottom: 1rem;
  padding: 1rem;
  background: #ffffff;
  box-shadow: 0px 0px 10px rgba(19, 19, 31, 0.05);
  border-radius: 5px;
}

/* first */
.date {
  display: flex;
  justify-content: space-between;
  margin-bottom: 1rem;
}

.date-font {
  font-family: 'Lexend Deca';
  color: #b6b6b6;
  font-size: 0.88rem;
}

/* second */
.title-font {
  font-size: 1.625rem;
  color: #313131;
  font-family: 'Lexend Deca';
  margin-bottom: 1rem;
}

/* third */
.content-font {
  font-family: 'Lexend Deca';
  color: #b6b6b6;
  font-size: 0.88rem;
}
</style>
