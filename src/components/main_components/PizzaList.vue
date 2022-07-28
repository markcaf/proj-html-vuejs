<template>
  <section class="my-5">
    <div class="heading text-center">
        <div class="subtitle mb-2">
            Choose your flavor
        </div>
        <h2 class="title text-uppercase mb-3">
            The best pizza menu in town
        </h2>
        <div class="description">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Suscipit consequuntur quod, nulla voluptas magnam quia cum? Tempora ullam similique eveniet molestiae ipsa accusamus saepe consectetur. Doloribus vel ipsum non nisi.
        </div>
    </div>

    <div class="wrapper_cards my-5 d-flex justify-content-between">
        <PizzaCard v-for="pizza in pizzas" :key="pizza.id"
        :imgUrl="pizza.src"
        :name="pizza.name"
        :price="pizza.price" />
    </div>

  </section>
</template>

<script>
import PizzaCard from './PizzaCard.vue';

export default {
    name: 'PizzaList',
    components: {
        PizzaCard,
    },

    data: function(){
        return{
            pizzas: [
                {
                    id: '1',
                    src: require('@/assets/img/h3-product-img-1a-100x100.png'),
                    name: 'Bismarck',
                    price: '30',
                },

                {
                    id: '2',
                    src: require('@/assets/img/h3-product-img-2a-150x150.png'),
                    name: 'Fiori di zucca',
                    price: '50',
                },

                {
                    id: '3',
                    src: require('@/assets/img/h3-product-img-3a-150x150.png'),
                    name: 'Campagnola',
                    price: '50',
                },

                {
                    id: '4',
                    src: require('@/assets/img/h3-product-img-4a-150x150.png'),
                    name: 'Pizza tartufata',
                    price: '45',
                },

                {
                    id: '5',
                    src: require('@/assets/img/h3-product-img-5a-150x150.png'),
                    name: 'Francescana',
                    price: '25',
                },

                {
                    id: '6',
                    src: require('@/assets/img/h3-product-img-6a-100x100.png'),
                    name: 'Valdostana',
                    price: '55',
                },
            ],
        }
    }

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

    section{
        overflow: hidden;

        .heading{
            max-width: 600px;
            margin: 0 auto;

            .subtitle{
                color: $btn_slider_text;
                font-size: 12px;
                font-weight: 500;
                text-transform: uppercase;
            }

            .title{
                font-size: 40px;
            }

            .description{
                color: $p_primary;
                font-family: sans-serif;
            }
        }

        .wrapper_cards{
            margin: 0 -100px;
        }
        
    }

</style>