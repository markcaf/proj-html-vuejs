<template>
  <header class="py-3">
    <div class="container-fluid">
        <div class="row d-flex justify-content-center align-items-center">
            <div class="col d-flex justify-content-end">
                <div class="red_button">
                    Order Online
                </div>
            </div>

            <div class="col text-end">
                <ul class="menu_sx list-unstyled">
                    <li>Home</li>
                    <li>Pages</li>
                    <li>Menu</li>
                </ul>
            </div>

            <div class="col-1 text-center">
                <img class="logo" src="../assets/img/h5-logo-divided-header.png" alt="Logo">
            </div>

            <div class="col text-start">
                <ul class="menu_dx list-unstyled">
                    <li>Event</li>
                    <li>Blog</li>
                    <li>Landing</li>
                </ul>
            </div>

            <div class="col">
                <ul class="navigation list-unstyled">
                    <li>
                        <img src="../assets/svg/svg-1.svg"  width="30" alt="" class="cart_icon">
                        Cart
                    </li>
                    <li>
                        <i class="fa-solid fa-magnifying-glass me-1"></i>
                        <span>Search</span>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    <Slider />
  </header>
</template>

<script>
import Slider from './Slider.vue';

export default {
    name: 'Header',
    components: {
        Slider,
    }

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

    header{
        background-color: $dark_bg;

        .red_button{
            color: white;
            padding: 8px 0;
            background-color: $red_bg;
            text-transform: uppercase;
            text-align: center;
            width: 150px;
            font-size: 13px;
            letter-spacing: 2px;
        }

        img{
            &.logo{
                width: 115px;
            }

            &.cart_icon{
                filter: invert(1);
                padding-bottom: 5px;
            }
        }

        ul{
            margin: auto 0;
            li{
                display: inline-block;
                margin: 0 20px;
                color: white;
                text-transform: uppercase;
                font-size: 13px;
                cursor: pointer;
                letter-spacing: 2px;
            }
        }

    }

</style>