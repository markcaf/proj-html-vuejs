<template>
  <main>
    <section id="image_cards" class="d-flex justify-content-between">
        <img src="../assets/img/h3-img-1.jpg" alt="">
        <img src="../assets/img/h3-img-1.jpg" alt="">
        <img src="../assets/img/h3-img-1.jpg" alt="">
        <img src="../assets/img/h3-img-1.jpg" alt="">
    </section>

  </main>
</template>

<script>

export default {
    name: 'Main',
    components: {

}

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
main{
    #image_cards{
        img{
            width: calc((100% / 4) - 8px);
            margin: 8px 0;
        }
    }
}
</style>