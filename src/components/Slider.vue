<template>
  <section class="my-5 d-flex justify-content-between align-items-center">
    <div class="prev-button" @click="previousPicture">
        Prev
    </div>

    <div class="content text-center">
        <!-- <img src="../assets/img/h3-rev-img-6.png" alt=""> -->
        <img :src="slides[activeImageIndex].image" :alt="Pizza" />
    </div>

    <div class="next-button" @click="nextPicture">
        Next
    </div>
  </section>
</template>

<script>
export default {
    name: 'Slider',

    data: function(){
        return{
            activeImageIndex: 0,

            autoPlay: null,

            slides: [
                {
                    image: require('@/assets/img/h3-rev-img-6.png'),
                    bg: require('@/assets/img/h3-rev-img-5.png'),
                },

                {
                    image: require('@/assets/img/h3-rev-img-4.png'),
                    bg: require('@/assets/img/h3-rev-img-3.png'),
                },

                {
                    image: require('@/assets/img/h3-rev-img-2.png'),
                    bg: require('@/assets/img/h3-rev-img-1.png'),
                }, 
            ],
        }
    },

    methods: {
        nextPicture: function () {
                if (this.activeImageIndex === this.slides.length - 1) {
                    this.activeImageIndex = 0;
                } else {
                    this.activeImageIndex++;
                };
            },

        previousPicture: function () {
            if (this.activeImageIndex === 0) {
                this.activeImageIndex = this.slides.length - 1;
            } else {
                this.activeImageIndex--;
            };
        },

        changePictureToIndex: function( indexToBeChanged ){
            this.activeImageIndex = indexToBeChanged;
        },
    }

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
            cursor: pointer;
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
            cursor: pointer;
        }
    }

</style>