<template>
<div class="container-fluid">
    <div class="row inner_wrap">
        <div class="col left d-flex align-items-center">
            <div class="content">
                <div class="heading mb-5">
                    <div class="subtitle mb-2">Made with love</div>
                    <h2 class="title text-uppercase mb-2 text-white">DELISH PIZZA DEALS</h2>
                </div>
                <infoCardEvent v-for="(event, index) in events" :key="index" 
                :day="event.day"
                :month="event.month"
                :name="event.name"
                />
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
    },

    data: function(){
        return{
            events: [
                {
                    day: '02',
                    month: 'Nov',
                    name: 'Traditional neapolitan pies in kyoto pizza mercato',
                },

                {
                    day: '03',
                    month: 'Nov',
                    name: 'Terarazza patio dining space opening this weekend',
                },

                {
                    day: '05',
                    month: 'Nov',
                    name: 'Sienna private dining room with stéphane brunn',
                },
            ],
        }
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