<template lang="pug">
  #Motorcycle.row.justify-center(style="margin-top: 50px;")
    .row.justify-center.items-center
      .grow-1.text-center
        img.moto-img.responsive(
          src="../assets/moto.jpg",
          alt="A single image"
        )
        a.txt-teal(href="https://github.com/fthiagogv")
          i.fa.fa-github.fa-3x
        a.txt-teal(href="https://linkedin.com/in/fthiagogv")
          i.fa.fa-linkedin-square.fa-3x
        a.txt-teal(href="https://twitter.com/fthiagogv")
          i.fa.fa-twitter-square.fa-3x

</template>
<script>
export default {
  name: 'Motorcycle'
}
</script>
<style lang="scss" scoped>
  img {
    filter: hue-rotate(115deg);
  }
</style>
