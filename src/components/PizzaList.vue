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
        <PizzaCard />
        <PizzaCard />
        <PizzaCard />
        <PizzaCard />
        <PizzaCard />
        <PizzaCard />
    </div>

  </section>
</template>

<script>
import PizzaCard from './PizzaCard.vue';

export default {
    name: 'PizzaList',
    components: {
        PizzaCard,
    }

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

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