<template>
  <div class="pizzacard text-center">
    <img src="../assets/img/h3-product-img-3a-150x150.png" alt="">
    <h5 class="title text-uppercase mt-4 mb-2">Nome Pizza</h5>
    <div class="price">$50.00</div>
  </div>
</template>

<script>
export default {
    name: 'PizzaCard',

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

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