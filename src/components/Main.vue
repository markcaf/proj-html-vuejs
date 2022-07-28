<template>
  <main>
    <section id="image_cards" class="d-flex justify-content-between gap-2">
        <imageCard v-for="image in imageCards" :key="image.id" 
        :imgUrl="image.src"/>
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
        <TeamCard v-for="card in teamCards" :key="card.id"
        :imgUrl="card.src" 
        :name="card.name"
        :role="card.role"
        />
    </section>

    <section id="partners" class="py-5 d-flex justify-content-center">
        <LogoPartner v-for="partner in partners" :key="partner.id"
        :imgUrl="partner.src" />
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
import imageCard from './main_components/imageCard.vue';
import SliderTestimonial from './main_components/SliderTestimonial.vue';
import TwoColumn from './main_components/TwoColumn.vue';
import Banner from './main_components/Banner.vue';
import TeamCard from './main_components/TeamCard.vue';
import LogoPartner from './main_components/LogoPartner.vue';
import PizzaList from './main_components/PizzaList.vue';
import TwoColumnEvent from './main_components/TwoColumnEvent.vue';
import BookTable from './main_components/BookTable.vue';

export default {
    name: 'Main',
    components: {
        imageCard,
        SliderTestimonial,
        TwoColumn,
        Banner,
        TeamCard,
        LogoPartner,
        PizzaList,
        TwoColumnEvent,
        BookTable,
    },

    data: function(){
        return{
            imageCards: [
                {
                    id: '1',
                    src: require('@/assets/img/h3-img-1.jpg'),
                },

                {
                    id: '2',
                    src: require('@/assets/img/h3-img-2.jpg'),
                },

                {
                    id: '3',
                    src: require('@/assets/img/h3-img-3.jpg'),
                },

                {
                    id: '4',
                    src: require('@/assets/img/h3-img-4.jpg'),
                },
            ],

            teamCards: [
                {
                    id: '1',
                    name: 'Mario Pizzella',
                    role: 'Head Chef',
                    src: require('@/assets/img/h1-team-1a-700x700.jpg'),
                },
                {
                    id: '2',
                    name: 'Margherita Olio',
                    role: 'Co-Chef',
                    src: require('@/assets/img/h1-team-2a.jpg'),
                },
                {
                    id: '3',
                    name: 'Frank Bailey',
                    role: 'Kitchen Porter',
                    src: require('@/assets/img/h1-team-4a.jpg'),
                },
                {
                    id: '4',
                    name: 'Anna Origano',
                    role: 'Sous Chef',
                    src: require('@/assets/img/h1-team-3a.jpg'),
                },
            ],

            partners: [
                {
                    id: '1',
                    src: require('@/assets/img/h1-clients-img-1.png'),
                },
                {
                    id: '2',
                    src: require('@/assets/img/h1-clients-img-2.png'),
                },
                {
                    id: '3',
                    src: require('@/assets/img/h1-clients-img-3.png'),
                },
                {
                    id: '4',
                    src: require('@/assets/img/h1-clients-img-4.png'),
                },
                {
                    id: '5',
                    src: require('@/assets/img/h1-clients-img-5.png'),
                },
            ],
        }
    }

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
main{
    // #image_cards{
    //     img{
    //         width: calc((100% / 4) - 8px);
    //         margin: 8px 0;
    //     }
    // }

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