<template>
<div class="container-fluid">
    <div class="row inner_wrap">
        <div class="col left d-flex justify-content-center align-items-center">
            <img src="../../assets/img/h1-img-7n.png" alt="">
        </div>

        <div class="col right d-flex align-items-center">
            <div class="content">
                <div class="heading">
                    <h2 class="title text-uppercase mb-2">SPECIALS*</h2>
                    <div class="subtitle">Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesent ut.</div>
                </div>
                <infoCard v-for="(card, index) in cards" :key="index"
                :price="card.price"
                :name="card.name"
                :description="card.description" 
                />
            </div>
        </div>
    </div>
</div>
</template>

<script>
import infoCard from './infoCard.vue';
export default {
    name: 'TwoColumn',
    components: {
        infoCard,
    },

    data: function(){
        return{
            cards: [
                {
                    price: '10',
                    name: 'Combo piccolo',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesent ut aliquam dui.',
                },
                {
                    price: '20',
                    name: 'Combo mezzo',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesent ut aliquam dui.',
                },
                {
                    price: '30',
                    name: 'Combo grande',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesent ut aliquam dui.',
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

        .left{
            background-image: url(../../assets/img/h1-img-4.jpg);
            background-size: cover;
            background-position: center;
        }

        .right{
            .content{
                padding-left: 25%;
                .heading{
                    max-width: 400px;
                    
                    .title{
                        font-size: 40px;
                    }

                    .subtitle{
                        color: $p_primary;
                        font-family: sans-serif;
                    }
                }
            }
        }

    }

</style>