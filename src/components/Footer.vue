<template>
  <footer>
    <div class="container-fluid">
      <div class="row inner_wrap">
          <div class="col left">
              <div class="menu_links d-flex gap-5">
                  <div class="menu">
                    <h5>Find our restaurants</h5>
                    <ul class="list-unstyled">
                      <Restaurant v-for="(restaurant, index) in restaurants" :key="index"
                      :address="restaurant.address"
                      :city="restaurant.city"
                      :tel="restaurant.tel"
                      />
                    </ul>
                  </div>

                  <div class="menu hours">
                    <h5>working hours</h5>
                    <ul class="list-unstyled">
                      <li>
                        <h5 class="day">Monday</h5>
                        <div class="close">Kitchen Closed</div>
                      </li>

                      <li>
                        <h5 class="day">Tuesday until friday</h5>
                        <div class="time">9:00 - 22:00</div>
                      </li>

                      <li>
                        <h5 class="day">Saturday</h5>
                        <div class="time">11am to midnight</div>
                      </li>

                      <li>
                        <h5 class="day">Sunday</h5>
                        <div class="time">9:00 - 22:00</div>
                      </li>
                    </ul>
                  </div>

                  <div class="text">
                    <div class="text-white text-uppercase">
                      THE DON PEPPE CREW FIRST AND FOREMOST VALUES AN AUTHENTIC, WELL BAKED SLICE OF PIZZA.
                    </div>
                  </div>
              </div>

              <div class="copyright d-flex align-items-end justify-content-between mx-4">
                <div class="text">
                  Created with <i class="fa-regular fa-heart"></i> <span>by Qode Interactive</span>
                </div>

                <div class="premium_logo">
                  <img src="../assets/img/footer-bottom-img.png" alt="">
                </div>
              </div>
            </div>

          <div class="col right">

        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Restaurant from './footer_components/Restaurant.vue';
export default {
    name: 'Footer',
    components: {
      Restaurant,
    },

    data: function(){
      return{
        restaurants: [
          {
            address: '1614 E. Bell Rd #104',
            city: 'Salerno, AZ 85022',
            tel: '(602) 867-1010',
          },

          {
            address: '204 E. Pizzetta Tommaso',
            city: 'Sorrento, AZ 85022',
            tel: '(358) 867-1010',
          },

          {
            address: 'Vale Puglia 54',
            city: 'Torre Del Greco AZ 85022',
            tel: '(359) 867-1010',
          },

          {
            address: 'Corso Italia',
            city: 'Naples, AZ 85022',
            tel: '(989) 867-1010',
          },
        ],
      }
    },

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

  footer{

    .inner_wrap{
      height: 700px;

      .right{
        background-image: url(../assets/img/footer-img-1.jpg);
        background-size: cover;
        background-position: center;
      }

      .left{
        background-image: url(../assets/img/h3-img-6.jpg);
        
        .menu_links{
          margin-top: 20%;
          padding-left: 20px;
          .menu{

            h5{
              color: $brown_text;
              text-transform: uppercase;
            }

            li{
              color: $p_primary;
              font-family: sans-serif;
              margin: 20px 0;
            }

            &.hours{
              margin: 0 30px;
              
              .day{
                text-transform: uppercase;
                font-size: 18px;
                font-family: 'Oswald', sans-serif;
              }

              .time{
                color: $p_primary;
                font-family: sans-serif;
              }

              .close{
                color: $dark_red;
              }
            }
          }

          .text{
            width: 30%;
            font-size: 25px;
          }
        }

        .copyright{
          margin-bottom: 40px;

          .text{
            color: $brown_text;

            span{
              color: $green_text;
            }
          }
        }
      }
    }

  }

</style>