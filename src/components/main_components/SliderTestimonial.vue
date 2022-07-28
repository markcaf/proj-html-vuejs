<template>
  <section class="my-5 d-flex justify-content-between align-items-center">
    <div class="prev-button" @click="previousPicture">
        Prev
    </div>

    <div class="content text-center">
        <div class="quote">“</div>
        <div class="testimonial_text">
            {{slides[activeImageIndex].text}}
        </div>
        <div class="testimonial_author">
            {{slides[activeImageIndex].author}}
        </div>

        <div class="navigation">
            <span class="dot active">
                <img src="../../assets/svg/svg-5.svg" width="8" alt="">
            </span>
            <span class="dot">
                <img src="../../assets/svg/svg-5.svg" width="8" alt="">
            </span>
            <span class="dot">
                <img src="../../assets/svg/svg-5.svg" width="8" alt="">
            </span>
        </div>
    </div>

    <div class="next-button" @click="nextPicture">
        Next
    </div>
  </section>
</template>

<script>
export default {
    name: 'SliderTestimonial',

    data: function(){
        return{
            activeImageIndex: 0,

            autoPlay: null,

            slides: [
                {
                    text: 'LOREM IPSUM DOLOR SIT AMET CONSECTETUR ADIPISICING ELIT. QUISQUAM EAQUE REICIENDIS REPUDIANDAE OFFICIA',
                    author: 'washington post 2018',
                },

                {
                    text: '“QUISQUAM EAQUE REICIENDIS REPUDIANDAE OFFICIA”',
                    author: 'los angeles post 2018',
                },

                {
                    text: '“LOREM IPSUM DOLOR SIT AMET CONSECTETUR ADIPISICING ELIT.”',
                    author: 'ny post 2018',
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
    },

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

    section{
        height: 300px;
        background-image: url(../../assets/img/h3-testimonials-bckgrnd.jpg);
        background-color: $testimonial_bg;
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;

        .content{
            max-width: 600px;

            .quote{
                font-size: 150px;
                color: $brown_text;
                font-weight: 500;
                line-height: 20px;
            }

            .testimonial_text{
                color: #303030;
                text-transform: uppercase;
                font-weight: 500;
                font-size: 25px;
            }

            .testimonial_author{
                color: $btn_slider_text;
                font-size: 12px;
                font-weight: 500;
                text-transform: uppercase;
            }

            .navigation{
                .dot{
                    filter: opacity(0.2);
                    margin: 0 5px;

                    &.active{
                        filter: invert(52%) sepia(69%) saturate(382%) hue-rotate(3deg) brightness(97%) contrast(89%);
                    }
                }
            }
        }

        .prev-button{
            writing-mode: vertical-rl;
            background-color: white;
            color: $btn_slider_text;
            padding-top: 20px;
            padding-bottom: 20px;
            padding-right: 5px;
            border-radius: 0 30px 30px 0;
            cursor: pointer;
        }

        .next-button{
            writing-mode: vertical-lr;
            background-color: white;
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