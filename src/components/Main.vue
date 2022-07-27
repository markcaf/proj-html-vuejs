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

    <section id="specials" class="my-2">
        <TwoColumn />
    </section>

    <section id="banner">
        <Banner />
    </section>

    <section id="team" class="d-flex mb-2">
        <TeamCard />
        <TeamCard />
        <TeamCard />
        <TeamCard />
    </section>

  </main>
</template>

<script>
import SliderTestimonial from './SliderTestimonial.vue';
import TwoColumn from './TwoColumn.vue';
import Banner from './Banner.vue';
import TeamCard from './TeamCard.vue';

export default {
    name: 'Main',
    components: {
        SliderTestimonial,
        TwoColumn,
        Banner,
        TeamCard,
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