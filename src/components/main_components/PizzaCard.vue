<template>
  <div class="pizzacard text-center">
    <img :src="imgUrl" :alt="name">
    <h5 class="title text-uppercase mt-4 mb-2">{{ name }}</h5>
    <div class="price">${{ price }}</div>
  </div>
</template>

<script>
export default {
    name: 'PizzaCard',

    props: {
        imgUrl: String,
        name: String,
        price: String,
    }

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

    .pizzacard{
        width: 200px;
        img{
            width: 100%
        };

        .title{
            color: $pizza_title;
        }

        .price{
            color: $pizza_price;
            font-size: 18px;
            font-weight: 500;
        }
    }

</style>