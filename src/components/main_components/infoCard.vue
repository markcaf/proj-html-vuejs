<template>
    <div class="infoCard">
        <div class="text_box d-flex gap-3">
            <div class="price">${{ price }}</div>
            <div class="info">
                <div class="name text-uppercase">{{ name }}</div>
                <div class="description">{{ description }}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'infoCard',

    props: {
        price: Number,
        name: String,
        description: String,
    },

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