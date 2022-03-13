<template>
  <footer class="footer">
    <b-row class="justify-content-center">
      <b-col class="d-flex justify-content-center">
        <div class="py-5">
          <div @click="scroll()">
            <b-img
              class="footer-icons"
              src="../assets/images/up-arrow.png"
              alt=""
            />
          </div>
        </div>
      </b-col>
    </b-row>
    <b-row class="justify-content-center">
      <b-col class="d-flex justify-content-center">
        <div>
          <a
            :href="bottomLink.href"
            target="_blank"
            v-for="bottomLink in bottomLinks"
            :key="bottomLink.title"
            ><img
              class="px-lg-5 px-2"
              :src="require(`../assets/images/${bottomLink.srcImage}.webp`)"
              :title="bottomLink.title"
          /></a>
        </div>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <hr />
        <div class="text-center text-white">
          <p>{{ madeBy }}</p>
        </div>
      </b-col>
    </b-row>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      madeBy: '© 2021 - Constantino Saldana',
      bottomLinks: [
        {
          title: 'Github',
          srcImage: 'github',
          href: 'https://github.com/antinomezco',
        },
        {
          title: 'Resumé',
          srcImage: 'cv',
          href: 'https://drive.google.com/file/d/1BN-iVteSjSrsRDsF62eaxipoa9kQPjBi/view?usp=sharing',
        },
        {
          title: 'LinkedIn',
          srcImage: 'linkedin',
          href: 'https://www.linkedin.com/in/constantinosaldana/?locale=en_US',
        },
      ],
    }
  },
  methods: {
    scroll() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth',
      })
    },
  },
}
</script>

<style scoped>
.footer {
  background-color: black;
}

.footer-icons {
  cursor: pointer;
}
</style>
