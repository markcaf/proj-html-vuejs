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

    <section id="partners" class="py-5 d-flex justify-content-center">
        <LogoPartner />
        <LogoPartner />
        <LogoPartner />
        <LogoPartner />
        <LogoPartner />
    </section>

    <section id="pizza_list" class="py-5">
        <PizzaList />
    </section>

    <section id="event" class="mb-2">
        <TwoColumnEvent />
    </section>

    <section id="book_a_table" class="py-5 mb-2 d-flex justify-content-center">
        <BookTable />
    </section>

  </main>
</template>

<script>
import SliderTestimonial from './SliderTestimonial.vue';
import TwoColumn from './TwoColumn.vue';
import Banner from './Banner.vue';
import TeamCard from './TeamCard.vue';
import LogoPartner from './LogoPartner.vue';
import PizzaList from './PizzaList.vue';
import TwoColumnEvent from './TwoColumnEvent.vue';
import BookTable from './BookTable.vue';

export default {
    name: 'Main',
    components: {
        SliderTestimonial,
        TwoColumn,
        Banner,
        TeamCard,
        LogoPartner,
        PizzaList,
        TwoColumnEvent,
        BookTable,
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

    #partners{
        background-color: $testimonial_bg;
    }

    #book_a_table{
        background-image: url(../assets/img/h3-background-img-3.jpg);
        background-position: center;
        background-size: cover;
    }
}
</style>