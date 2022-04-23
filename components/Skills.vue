<template>
  <section class="skills-container">
    <b-row>
      <b-col class="text-center">
        <p class="title-text pb-3" id="skills">Skills</p>
        <p class="regular-text p-2">
          Besides the usual JavaScript, HTML and CSS skills...
        </p>
      </b-col>
    </b-row>
    <b-row class="justify-content-center">
      <b-col lg="6" md="8" sm="10" cols="12" class="text-center">
        <div class="d-flex flex-wrap">
          <div v-for="skill in skills" :key="skill.title" class="m-auto">
            <b-link target="_blank" class="p-3" :href="skill.web">
              <b-img
                height="100"
                weight="100"
                :src="skill.imageSrc"
                :alt="skill.alt"
                :title="skill.alt"
              />
            </b-link>
            <p class="p-2 font-weight-bold">{{ skill.alt }}</p>
          </div>
        </div>
        <BaseScrollTo desc="Who Am I?" variantColor="primary" descendTo="photo" />
      </b-col>
    </b-row>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        { title: 'vue', imageSrc: 'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591600/portfolio/vue_n7qtcp.webp',  alt: 'Vue.js', web: 'https://vuejs.org/v2/guide/' },
        { title: 'react', imageSrc: 'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591602/portfolio/react_hcpoe2.webp', alt: 'React', web: 'https://reactjs.org/' },
        { title: 'strapi', imageSrc: 'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591607/portfolio/strapi_deuotd.webp', alt: 'Strapi', web: 'https://strapi.com/' },
        { title: 'bootstrap-vue', imageSrc: 'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591600/portfolio/bootstrap-vue_q7fyzn.webp', alt: 'BootstrapVue', web: 'https://bootstrap-vue.org/' },
        { title: 'tailwind-css', imageSrc: 'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591599/portfolio/tailwind-css_f1vrfx.webp', alt: 'TailwindCSS', web: 'https://tailwindcss.com/' },
        {
          title: 'django',
           imageSrc: 'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591600/portfolio/django_mzdylu.webp',
          alt: 'Django',
          web: 'https://learndjango.com/tutorials/what-django-python',
        },
        { title: 'graphql', imageSrc: 'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591601/portfolio/graphql_udouht.webp', alt: 'GraphQL', web: 'https://graphql.org/' },
        {
          title: 'postgres', imageSrc: 'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591601/portfolio/postgres_fgvqyf.webp',
          alt: 'PostgreSQL',
          web: 'https://www.postgresql.org/about/',
        },
        { title: 'git', imageSrc: 'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591600/portfolio/git_gyto0o.webp', alt: 'Git', web: 'https://git-scm.com/' },
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
