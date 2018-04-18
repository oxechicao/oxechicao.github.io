<template lang="pug">
  #Themes.row.justify-center(style="padding: 50px;")
    .row.justify-center
      .grow-1
        .row.justify-center.items-center.wrapper
          .grow-1.text-center
            h1 Temas para editores:
        .row.justify-center.items-center.wrapper
          .grow-1.text-center
            a(href="https://marketplace.visualstudio.com/items?itemName=fthiagogv.NatureRainbow-Theme")
              h3 Nature Rainbow (VS Code)
              img(
                src='https://user-images.githubusercontent.com/6399202/30041107-93830984-91bd-11e7-9257-81d293c46714.png'
              )

        .row.justify-center.items-center.wrapper
          .grow-1.text-center
            a(href="https://atom.io/themes/naturegreen-dark-syntax")
              h3 Nature Green Dark (Atom)
              img(
                src='https://user-images.githubusercontent.com/6399202/27262521-803da1bc-542e-11e7-9b3a-c6cd16dbb339.png'
              )


          .grow-1.text-center
            a(href="https://atom.io/themes/naturegreen-light-syntax")
              h3 Nature Green Light (Atom)
              img(
                src='https://user-images.githubusercontent.com/6399202/27262513-641b97a0-542e-11e7-9a72-2432fcf5381e.png'
              )

        .row.justify-center.items-center.wrapper
          .grow-1.text-center
            a(href="https://github.com/fthiagogv/naturepurple-dark-syntax")
              h3 Nature Purple (Atom)
              img(
                src='https://cloud.githubusercontent.com/assets/6399202/8514658/c6724cb0-236a-11e5-91cb-f0f528255287.jpg'
              )

          .grow-1.text-center
            a(href="https://atom.io/themes/naturerainbow-dark-syntax")
              h3 Nature Rainbow (Atom)
              img(
                src='https://user-images.githubusercontent.com/6399202/30009975-e7092b62-9102-11e7-8d74-f8654b3f274c.png'
              )

</template>
<script>
export default {
  name: 'Themes'
}
</script>
<style scoped>
.text-center {
  margin: 0px 30px 0px 30px;
}
h1, h2, h3, a {
  color: gray;
}
a img {
  height: 200px;
}
</style>

