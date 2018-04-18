<template lang="pug">
#Home
  .body-container
    div
      img.moto-img(
        src="../assets/moto.jpg",
        alt="A single image",
        width="300px",
        style="filter: hue-rotate(120deg);"
      )
      h3 Thiago Gomes, Chicão
    div
      small
        a.social.txt-teal(href="https://github.com/fthiagogv")
          i.fa.fa-github.fa-3x
        a.social.txt-teal(href="https://linkedin.com/in/fthiagogv")
          i.fa.fa-linkedin-square.fa-3x
        a.social.txt-teal(href="https://twitter.com/fthiagogv")
          i.fa.fa-twitter-square.fa-3x
    div(style="margin-top: 30px;")
      a(style="margin: 10px;", @click="showAbout") .me
      a(style="margin: 10px;", @click="showProjects") .projects
      a(style="margin: 10px;", @click="showThemes") .editorThemes

    div(style="margin-top: 50px;")
      .content-body(v-if="projects")
        a(target="_blank", href="https://fthiagogv.github.io/image-to-pdf/")
          p Image to pdf (Vuejs)
      .content-body(v-if="themes")
        a(target="_blank", href="https://marketplace.visualstudio.com/items?itemName=fthiagogv.NatureRainbow-Theme")
          p Nature Rainbow (VS Code)
        a(target="_blank", href="https://atom.io/themes/naturegreen-dark-syntax")
          p Nature Green Dark (Atom)
        a(target="_blank", href="https://atom.io/themes/naturegreen-light-syntax")
          p Nature Green Light (Atom)
        a(target="_blank", href="https://github.com/fthiagogv/naturepurple-dark-syntax")
          p Nature Purple (Atom)
        a(target="_blank", href="https://atom.io/themes/naturerainbow-dark-syntax")
          p Nature Rainbow (Atom)
      .content-body(v-if="about")
          p I'm a brazilian developer that love what I do.
          p A master degree student at
            a(target="_blank", href="https://uece.br/macc")
              b
                i  UECE (Universidade Estadual do Ceará, Brazil)
            | . I'm studying about serverless, microservices, self-adaptive, distributed systems, resource allocation, etc.
          p Currently I working as Fullstack Developer, with Vuejs and a little bit of Laravel.

</template>

<script>
export default {
  name: 'Home',
  components: {
  },
  data () {
    return {
      projects: false,
      themes: false,
      about: true
    }
  },
  methods: {
    showProjects () {
      this.offAll()
      this.projects = !this.projects
    },
    showThemes () {
      this.offAll()
      this.themes = !this.themes
    },
    showAbout () {
      this.offAll()
      this.about = !this.about
    },
    offAll () {
      this.projects = false
      this.themes = false
      this.about = false
    }
  },
  computed: {
    showContent: function () {
      return this.projects || this.themes || this.about
    }
  }

}
</script>

<style scoped>
a {
  text-decoration: none;
  color: hsl(150, 40%, 50%);
}
.body-container {
  margin-top: 30px;
  text-align: center;
  color: hsl(150, 40%, 50%);
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
  height: 100vh;
}
.vl {
  border-left: 1px solid hsla(150, 50%, 50%, 0.3);
  margin-left: 50px;
  margin-right: 50px;
}
.social {
  margin: 10px;
}
.content-body {
  max-width: 650px;
  min-width: 300px;
  text-align: left;
  margin-left: 10px;
  margin-right: 10px;
}
</style>
A master degree student on UECE. I'm studying about serverless, microservices, self-adaptive, distributed systems, resource allocation, etc.

