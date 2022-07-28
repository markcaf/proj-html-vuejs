<template>
    <div class="infoCard">
        <div class="text_box d-flex gap-3">
            <div class="date">
                <div class="day">02</div>
                <div class="month text-white text-center">Nov</div>
            </div>
            <div class="info">
                <div class="name text-white text-uppercase pt-1 mb-2">Traditional neapolitan pies in kyoto pizza mercato</div>
                <div class="description">
                    <i class="fa-solid fa-location-dot"></i>
                    204 E. Pizzetta Tommaso</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'infoCardEvent',

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
    .infoCard{
        max-width: 400px;
        margin: 25px 0;

        .text_box{
            .date{
                .day{
                    color: $dark_red;
                    font-size: 50px;
                    font-weight: 500;
                    line-height: 55px;
                }

                .month{
                    font-size: 20px;
                    text-transform: uppercase;
                }
            }

            .info{
                .name{
                    font-size: 20px;
                    font-weight: 500;
                    line-height: 30px;
                }

                .description{
                    color: $dark_red;
                    font-family: sans-serif;
                    font-size: 14px;
                }
            }
        }
    }
</style>