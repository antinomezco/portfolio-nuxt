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
      <b-col lg="5" md="6" cols="12">
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
          name: 'recipe',
          title: 'Recipe Database (frontend)',
          link: 'https://agitated-hermann-0d809c.netlify.app/',
          source: 'https://github.com/antinomezco/calaveria',
          tech: 'VueJS, Firebase, Auth0',
          desc: 'I love cooking, so I created a simple searchable recipe website for myself so I can store my favorite recipes and share them with my friends/family. Website was made using VueJS with authentication through Auth0. Dynamically created recipe pages, CRUD and image storage through Firebase storage buckets available.',
        },
        {
          id: 2,
          name: 'reciperest',
          title: 'Recipe Database (backend)',
          link: '',
          source: 'https://github.com/antinomezco/cookingdb',
          tech: 'Django, Postgres, Rest',
          desc: 'I wanted a place to store my recipes and not have them fixed in code, so I used Django API for use in the Recipe Database (frontend) since Python is easy to understand. Allows for REST CRUD connection for users and recipes.',
        },
        {
          id: 3,
          name: 'portfolio',
          title: 'Portfolio page',
          link: 'https://www.csaldana.xyz',
          source: 'https://github.com/antinomezco/portfolio2021',
          tech: 'VueJS, Boostrap-vue',
          desc: 'I wanted a simple portfolio page to show my skills using only HTML, CSS, Nuxt (VueJS) and Boostrap-vue.',
        },
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
