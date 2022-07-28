<template>
    <div class="infoCard">
        <div class="text_box d-flex gap-3">
            <div class="price">$10</div>
            <div class="info">
                <div class="name">COMBO PICCOLO</div>
                <div class="description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesent ut aliquam dui.</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'infoCard',

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
    .infoCard{
        max-width: 400px;
        margin: 25px 0;

        .text_box{
            .price{
                color: $dark_red;
                font-size: 25px;
                font-weight: 500;
            }

            .info{
                .name{
                    font-size: 25px;
                    font-weight: 500;
                }

                .description{
                    color: $p_secondary;
                    font-family: sans-serif;
                    font-size: 14px;
                }
            }
        }
    }
</style>