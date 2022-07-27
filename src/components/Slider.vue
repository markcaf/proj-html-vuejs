<template>
  <section class="my-5 d-flex justify-content-between align-items-center">
    <div class="prev-button">
        Prev
    </div>

    <div class="content text-center">
        <img src="../assets/img/h3-rev-img-6.png" alt="">
    </div>

    <div class="next-button">
        Next
    </div>
  </section>
</template>

<script>
export default {
    name: 'Slider',

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

    section{
        height: 300px;
        background-image: url(../assets/img/h3-rev-img-5.png);
        background-size: contain;
        background-position: center;
        background-repeat: no-repeat;

        .content{
            img{
                width: 75%;
            }
        }

        .prev-button{
            writing-mode: vertical-rl;
            background-color: $btn_slider_bg;
            color: $btn_slider_text;
            padding-top: 20px;
            padding-bottom: 20px;
            padding-right: 5px;
            border-radius: 0 30px 30px 0;
        }

        .next-button{
            writing-mode: vertical-lr;
            background-color: $btn_slider_bg;
            color: $btn_slider_text;
            padding-top: 20px;
            padding-bottom: 20px;
            padding-right: 5px;
            border-radius: 0 30px 30px 0;
            -moz-transform: scale(-1, -1);
            -webkit-transform: scale(-1, -1);
            -o-transform: scale(-1, -1);
            -ms-transform: scale(-1, -1);
            transform: scale(-1, -1);
        }
    }

</style>