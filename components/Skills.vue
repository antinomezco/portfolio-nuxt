<template>
  <section class="skills-container">
    <b-row class="justify-content-center">
      <b-col lg="6" md="8" sm="10" cols="12" class="text-center">
        <p class="title-text pb-3" id="skills">Skills</p>
        <p class="regular-text pb-2">
          Besides the usual JavaScript, HTML and CSS skills...
        </p>
        <div class="d-flex flex-wrap">
          <div v-for="skill in skills" :key="skill.title" class="m-auto">
            <b-link target="_blank" class="p-3" :href="skill.web">
              <b-img
                
                height="100"
                weight="100"
                :src="require(`../assets/images/${skill.title}.webp`)"
                :alt="skill.alt"
                :title="skill.alt"
              />
            </b-link>
            <p class="p-2 font-weight-bold">{{ skill.alt }}</p>
          </div>
        </div>
        <ScrollTo desc="Who Am I?" variantColor="primary" descendTo="photo" />
      </b-col>
    </b-row>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        { title: 'vue', alt: 'Vue.js', web: 'https://vuejs.org/v2/guide/' },
        { title: 'react', alt: 'React', web: 'https://reactjs.org/' },
        { title: 'strapi', alt: 'Strapi', web: 'https://strapi.com/' },
        { title: 'bootstrap-vue', alt: 'BootstrapVue', web: 'https://bootstrap-vue.org/' },
        {
          title: 'django',
          alt: 'Django',
          web: 'https://learndjango.com/tutorials/what-django-python',
        },
        { title: 'graphql', alt: 'GraphQL', web: 'https://graphql.org/' },
        {
          title: 'postgres',
          alt: 'PostgreSQL',
          web: 'https://www.postgresql.org/about/',
        },
        { title: 'git', alt: 'Git', web: 'https://git-scm.com/' },
      ],
    }
  },
}
</script>

<style scoped>
.skills-container {
  background-color: orange;
  padding: 200px 0 100px;
  -webkit-clip-path: polygon(0 12%, 100% 0%, 100% 100%, 0 100%);
  clip-path: polygon(0 12%, 100% 0%, 100% 100%, 0 100%);
}
</style>
