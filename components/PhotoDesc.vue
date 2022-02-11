<template>
  <section class="hero" id="photo">
    <h2 class="text-center title-text text-white">Who am I?</h2>
    <b-row class="d-flex justify-content-center">
      <b-col lg="3" md="5" sm="6" cols="6" class="d-flex justify-content-center justify-content-md-end py-4">
        <ImageComponent />
      </b-col>
      <b-col lg="4" md="6" sm="8" cols="10" class="d-flex align-items-center">
        <p class="font-weight-bold text-white regular-text">I'm Constantino, a trilingual (English, French and Spanish) Full Stack developer based in Montreal, specializing in web development using VueJS as a frontend alongside Django as an API backend or Strapi as a headless CMS.</p>
      </b-col>
    </b-row>
    <ScrollTo desc="Check out my projects" variantColor="outline-light" descendTo="projects"/>
  </section>
</template>

<style scoped>
.hero {
  background-color: black;
  padding-bottom: 200px;
  padding-top: 100px;
  -webkit-clip-path: polygon(0 0, 100% 0%, 100% 100%, 0 79%);
  clip-path: polygon(0 0, 100% 0%, 100% 100%, 0 79%);
}
</style>
