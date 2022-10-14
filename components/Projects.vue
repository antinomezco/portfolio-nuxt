<template>
  <section class="px-5">
    <b-row class="justify-content-center">
      <b-col
        lg="6"
        md="8"
        sm="10"
        cols="12"
      >
        <p
          class="text-center title-text pb-3"
          id="projects"
        >
          Projects and/or Experience
        </p>
      </b-col>
    </b-row>
    <b-row
      v-for="box in boxes"
      :key="box.name"
      class="boxes pb-5 justify-content-center"
    >
      <b-col
        lg="5"
        md="6"
        cols="12"
        class="d-flex flex-column justify-content-center"
      >
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
            <b-button
              variant="outline-dark"
              class="link-text mr-2 mr-lg-5 purple"
              :href="box.link"
              target="_blank"
            >Live demo</b-button>
          </div>
          <div v-if="box.source">
            <b-button
              variant="link"
              class="font-size-biggish link-text text-decoration-none"
              :href="box.source"
              target="_blank"
            >
              Source Code
            </b-button>
          </div>
        </div>
      </b-col>
      <b-col
        lg="5"
        md="6"
        sm="12"
        cols="12"
        class="pt-3"
      >
        <div class="" style="border: 5px solid black; border-radius: 9px;">
          <a
            :href="box.link"
            target="_blank"
          >
            <b-img
              fluid-grow
              rounded
              :src="box.imageSrc"
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
          name: 'workstaff',
          imageSrc:
            'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591601/portfolio/magazine_nufzwg.jpg',
          title: 'Workstaff',
          link: 'https://workstaff.app',
          source: '',
          tech: 'React (Docusaurus), Angular',
          desc: 'Customized their Docusaurus blog and built Angular components by using internal reusable components and RxJS observables.',
        },
        {
          id: 1,
          name: 'magazine',
          imageSrc:
            'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591601/portfolio/magazine_nufzwg.jpg',
          title: 'Le Centre franco-ontarien de ressources pédagogiques',
          link: 'https://numerico.cforp.ca/magazines',
          source: '',
          tech: 'VueJS (Nuxt), Boostrap-vue, Tailwind, Strapi',
          desc: 'Built QUAD9 and Mon Mag À Moi magazine articles using Bootstrap-vue and Tailwind. Created strapi backend to dynamically reuse magazine article templates.',
        },
        {
          id: 2,
          name: 'ecommerce',
          imageSrc:
            'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650743280/portfolio/ecommerce_ieqba2_xolmnl.png',
          title: 'Audiophile e-commerce website',
          link: 'https://ecommerce-example-contentful.vercel.app/',
          source: 'https://github.com/antinomezco/ecommerce-example-contentful',
          tech: 'React (Next), Tailwind, Contentful',
          desc: 'My first Next.js project. Fully responsive fake e-commerce website in which you can browse through the categories/products, add and remove items from the cart state, form validation for payment and more. Using Contentful as a backend for images and text.',
        },
        {
          id: 3,
          name: 'recipe',
          imageSrc:
            'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591616/portfolio/recipe_d9wj3r.png',

          title: 'Recipe Database (frontend)',
          link: 'https://agitated-hermann-0d809c.netlify.app/',
          source: 'https://github.com/antinomezco/calaveria',
          tech: 'VueJS (Nuxt), Firebase, Auth0, Tailwind',
          desc: 'Searchable recipe website to store my favorite recipes and share them with my friends/family. Website was made using VueJS with authentication through Auth0. Dynamically created recipe pages, CRUD and image storage through Firebase storage buckets available.',
        },
        {
          id: 4,
          name: 'reciperest',
          imageSrc:
            'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591605/portfolio/reciperest_frhqfq.png',

          title: 'Recipe Database (backend)',
          link: '',
          source: 'https://github.com/antinomezco/cookingdb',
          tech: 'Django, Postgres, Rest',
          desc: 'Django server used an an API for the above Recipe Database. Allows for REST CRUD connections for users and recipes.',
        },
        {
          id: 5,
          name: 'spacetourism',
          imageSrc:
            'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591610/portfolio/spacetourism_jeoao9.png',

          title: 'Space Tourism',
          link: 'https://thirsty-archimedes-a0d572.netlify.app/',
          source: 'https://github.com/antinomezco/space-tourism-nuxt',
          tech: 'VueJS (Nuxt), Tailwind',
          desc: 'Simple landing page for improving my skills using Tailwind.',
        },
        {
          id: 6,
          name: 'portfolio',
          title: 'Portfolio page',
          imageSrc:
            'https://res.cloudinary.com/dlgsjm7jt/image/upload/v1650591602/portfolio/portfolio_amjro8.png',

          link: 'https://www.csaldana.xyz',
          source: 'https://github.com/antinomezco/portfolio-nuxt',
          tech: 'VueJS (Nuxt), Boostrap-vue',
          desc: 'Portfolio page to show my skills. Inspired by the Simplefolio template.',
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
