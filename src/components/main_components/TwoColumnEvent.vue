<template>
<div class="container-fluid">
    <div class="row inner_wrap">
        <div class="col left d-flex align-items-center">
            <div class="content">
                <div class="heading mb-5">
                    <div class="subtitle mb-2">Made with love</div>
                    <h2 class="title text-uppercase mb-2 text-white">DELISH PIZZA DEALS</h2>
                </div>
                <infoCardEvent />
                <div class="separator"></div>
                <infoCardEvent />
                <div class="separator"></div>
                <infoCardEvent />
            </div>
        </div>

        <div class="col right">

        </div>
    </div>
</div>
</template>

<script>
import infoCardEvent from './infoCardEvent.vue';
export default {
    name: 'TwoColumnEvent',
    components: {
        infoCardEvent,
    }
}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

    .inner_wrap{
        height: 700px;

        .right{
            background-image: url(../../assets/img/h3-img-5a.jpg);
            background-size: cover;
            background-position: center;
        }

        .left{
            background-image: url(../../assets/img/h3-img-6.jpg);
            .content{
                padding-left: 25%;

                .separator{
                    border-top: 2px dotted #b7903c;
                }

                .heading{
                    max-width: 400px;
                    
                    .title{
                        font-size: 40px;
                    }

                    .subtitle{
                        color: $subtitle_event;
                        font-size: 12px;
                        font-weight: 500;
                        text-transform: uppercase;
                    }
                }
            }
        }

    }

</style>