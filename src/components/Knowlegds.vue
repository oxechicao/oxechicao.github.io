<template lang="pug">
  #Knowlegds.row.justify-center.txt-teal(style="padding: 30px;")
    .row.justify-center
      .grow-1
        .row.justify-center.items-center
          .grow-1.text-center
            h2 Algumas das expertises usadas no dia a dia:

        .row.justify-center.items-center(style="min-width: 300px;")
          .grow-1.text-center
            img(
              src="https://github.com/laravel/art/raw/master/laravel-l-slant.png",
              title="Laravel"
            )
          .grow-1.text-center
            img(
              src="../assets/logo.svg",
              style="width: 100px;"
              title="Vuejs"
            )
          .grow-1.text-center
            img(
              src="https://nodejs.org/static/images/logos/nodejs-new-pantone-black.png",
              title="NodeJs"
            )
          .grow-1.text-center
            img(
              src="https://github.com/pugjs/pug-logo/raw/master/PNG/pug-final-logo_-colour-512.png",
              title="Pugjs"
            )
          .grow-1.text-center
            img(
              src="https://assets-cdn.github.com/images/modules/logos_page/Octocat.png",
              title="Git",
            )

</template>
<script>
export default {
  name: 'Knowlegds'
}
</script>
<style scoped>
  .img-sab, img {
    max-width: 100px;
  }
  img {
    margin: 30px;
  }
</style>
