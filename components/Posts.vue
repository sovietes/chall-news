<template>
  <section class="posts">
    <div v-for="post in posts" :key="post.title" v-scroll-reveal>
      <Card :date="post.date" :title="post.title" :content="post.content" />
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      posts: [
        {
          date: '02 de jul, 2021',
          title: 'Agora é oficial: o Windows 11 está vindo',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum vestibulum auctor est. Nam vitae finibus ante. Duis lobortis tellus vel diam fringilla, eu ullamcorper ex iaculis.',
        },
        {
          date: '02 de jul, 2021',
          title: 'Tim Berners-Lee vai leiloar código-fonte da web',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum vestibulum auctor est. Nam vitae finibus ante. Duis lobortis tellus vel diam fringilla, eu ullamcorper ex iaculis. Praesent et auctor justo. Vestibulum nisl orci, lacinia venenatis leo sit amet, pulvinar tincidunt risus. Phasellus nisl dui, cursus a lectus et, interdum ullamcorper libero.',
        },
        {
          date: '02 de jul, 2021',
          title: 'Tem Firefox novo no pedaço e você vai querer migrar',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum vestibulum auctor est.',
        },
        {
          date: '02 de jul, 2021',
          title: 'John McAfee, criador do antivírus McAfee, morre',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum vestibulum auctor est. Nam vitae finibus ante. Duis lobortis tellus vel diam fringilla, eu ullamcorper ex iaculis. Praesent et auctor justo. Vestibulum nisl orci, lacinia venenatis leo sit amet, pulvinar tincidunt risus. Phasellus nisl dui, cursus a lectus et, interdum ullamcorper libero.',
        },
      ],
    }
  },
})
</script>

<style scoped>
.posts {
  max-width: 1100px;
  width: 100%;
  margin: 0 auto;
  margin-top: 3rem;
  padding: 0.5rem 2rem;
}
</style>
