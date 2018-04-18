<template lang="pug">
  #TopMenu.bg-teal
    .row.wrap.items-center
      .grow-1.text-left(style="margin-left: 15px; color: lightcyan")
        a(
          href="https://fthiagogv.github.io"
        )
          img(
            src="https://avatars0.githubusercontent.com/u/6399202?v=4&s=460"
          )
          b F. Thiago Gomes V.
          small
            i  (página em desenvolvimento)

      //- .grow-1.text-right
        ul.txt-common-d
          li
            a(href="#") Inicio
          li
            a(href="#") Projetos
          li
            a(href="#") Temas
          li
            a(href="#") Sobre
</template>
<script>
export default {
  name: 'TopMenu'
}
</script>

<style scoped>
  #TopMenu {
    min-height: 50px;
    line-height: 50px;
  }

  a {
    color: inherit;
    text-decoration: inherit;
  }

  img {
    filter: sepia(50%);
    vertical-align: middle;
    margin-right: 20px;
    margin-left: 20px;
    max-width: 40px;
    max-height: 40px;
    border-radius: 5px;
  }

  ul {
    list-style-type: none;
    margin: 0px;
    padding: 0px;
  }
  li {
    display: inline;
  }
  li a {
    text-decoration: none;
    color: lightcyan;
    padding: 16px;
  }
  li a:hover {
    text-decoration: none;
    color: aquamarine;
    background: teal;
  }
</style>
