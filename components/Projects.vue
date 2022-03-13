<template>
  <section class="Projects px-5">
    <b-row class="justify-content-center">
      <b-col lg="6" md="8" sm="10" cols="12">
        <p class="text-center title-text pb-3" id="projects">
          Projects and/or Experience
        </p>
      </b-col>
    </b-row>
    <b-row v-for="box in boxes" :key="box.name" class="boxes pb-5 justify-content-center">
      <b-col lg="5" md="6" cols="12" class="d-flex flex-column justify-content-center">
        <div class="font-size-biggish purple">
          {{ box.title }}
        </div>
        <div class="regular-text">
          <p>
            {{ box.desc }}
          </p>
          <p>
            Technologies used: <span> {{ box.tech }}</span>
          </p>
        </div>
        <div class="d-flex align-items-center">
          <div v-if="box.link">
            <b-button variant="outline-dark" class="link-text mr-2 mr-lg-5 purple" :href="box.link" target="_blank">Live demo</b-button>
          </div>
          <div v-if="box.source">
            <b-button variant="link" class="font-size-biggish link-text text-decoration-none" :href="box.source" target="_blank">
              Source Code
            </b-button>
          </div>
        </div>
      </b-col>
      <b-col lg="5" md="6" sm="12" cols="12" class="pt-3">
        <div class="">
          <a :href="box.link" target="_blank">
            <b-img
              thumbnail
              fluid-grow
              rounded
              :src="require(`../assets/images/${box.name}.png`)"
              alt=""
            />
          </a>
        </div>
      </b-col>
    </b-row>
  </section>
</template>

<script>
export default {
  data() {
    return {
      boxes: [
        {
          id: 1,
          name: 'magazine',
          title: 'Le Centre franco-ontarien de ressources pédagogiques',
          link: 'https://numerico.cforp.ca/magazines',
          source: '',
          tech: 'VueJS (Nuxt), Boostrap-vue, Tailwind, Strapi',
          desc: 'Built QUAD9 and Mon Mag À Moi magazine articles using Bootstrap-vue and Tailwind. Created strapi backend to dynamically reuse magazine article templates.',
        },
        {
          id: 2,
          name: 'recipe',
          title: 'Recipe Database (frontend)',
          link: 'https://agitated-hermann-0d809c.netlify.app/',
          source: 'https://github.com/antinomezco/calaveria',
          tech: 'VueJS (Nuxt), Firebase, Auth0, Tailwind',
          desc: 'Searchable recipe website to store my favorite recipes and share them with my friends/family. Website was made using VueJS with authentication through Auth0. Dynamically created recipe pages, CRUD and image storage through Firebase storage buckets available.',
        },
        {
          id: 3,
          name: 'reciperest',
          title: 'Recipe Database (backend)',
          link: '',
          source: 'https://github.com/antinomezco/cookingdb',
          tech: 'Django, Postgres, Rest',
          desc: 'API for use in the above Recipe Database. Allows for REST CRUD connections for users and recipes.',
        },
        {
          id: 4,
          name: 'portfolio',
          title: 'Portfolio page',
          link: 'https://www.csaldana.xyz',
          source: 'https://github.com/antinomezco/portfolio-nuxt',
          tech: 'VueJS (Nuxt), Boostrap-vue',
          desc: 'Portfolio page to show my skills. Inspired by the Simplefolio template.',
        }
      ],
    }
  },
}
</script>

<style scoped>
.font-size-biggish {
  font-size: 1.3rem;
}
</style>
