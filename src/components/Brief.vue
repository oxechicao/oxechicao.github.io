<template lang="pug">
  #Brief.row.justify-center
    .row.justify-center
      .grow-1
        .row.justify-center.items-center.wrapper
          .grow-1.text-center(style="width: 50%; margin-left: 50px;")
            p.textBrief.txt-teal
              b Francisco Thiago Gomes Vieira,
              br
              |  é um mestrando em Ciência da Computação na Universidade Estadual do Ceará
              br
              |  e desenvolvedor Full Stack (ou busca ser) pelo prazer de codificar diariamente ;)


        .row.justify-center
          div.social-icons.txt-teal
            a.txt-teal(href="https://github.com/fthiagogv")
              i.fa.fa-github.fa-3x
            a.txt-teal(href="https://linkedin.com/in/fthiagogv")
              i.fa.fa-linkedin-square.fa-3x
            a.txt-teal(href="https://twitter.com/fthiagogv")
              i.fa.fa-twitter-square.fa-3x
            a.txt-teal(href="https://facebook.com/fthiagogv")
              i.fa.fa-facebook-square.fa-3x
            a.txt-teal(href="https://instagram.com/fthiagogv")
              i.fa.fa-instagram.fa-3x
            a.txt-teal(href="mailto:fthiagogv@gmail.com")
              i.fa.fa-envelope-square.fa-3x

</template>
<script>
export default {
  name: 'Brief'
}
</script>
<style lang="scss" scoped>
#Brief {
  padding: 100px;
}
  .profile {
    max-width: 150px;
    border-radius: 30px;
  }
  .textBrief {
    font-size: 25px;
  }
  .social-icons i {
    margin: 20px;
  }
</style>
