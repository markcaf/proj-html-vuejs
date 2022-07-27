<template>
  <main>
    <section id="image_cards" class="d-flex justify-content-between">
        <img src="../assets/img/h3-img-1.jpg" alt="">
        <img src="../assets/img/h3-img-1.jpg" alt="">
        <img src="../assets/img/h3-img-1.jpg" alt="">
        <img src="../assets/img/h3-img-1.jpg" alt="">
    </section>

    <section id="testimonial_slider">
        <SliderTestimonial />
    </section>

    <section id="specials">
        <TwoColumn />
    </section>

  </main>
</template>

<script>
import SliderTestimonial from './SliderTestimonial.vue';
import TwoColumn from './TwoColumn.vue';

export default {
    name: 'Main',
    components: {
        SliderTestimonial,
        TwoColumn,
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

    #testimonial_slider{
        padding: 10px 0;
        background-color: $testimonial_bg;
    }
}
</style>