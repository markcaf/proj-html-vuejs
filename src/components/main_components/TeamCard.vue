<template>
  <div class="team_card">
    <img class="photo" :src="imgUrl" alt="">

    <div class="info_user">
      <div class="wrapper text-white">
        <h5 class="name text-center text-uppercase">{{name}}</h5>
        <div class="role text-center">{{role}}</div>
        <div class="social d-flex justify-content-center gap-3">
          <i class="fa-brands fa-instagram"></i>
          <i class="fa-brands fa-twitter"></i>
          <i class="fa-brands fa-facebook"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'TeamCard',

    props: {
      id: String,
      imgUrl: String,
      name: String,
      role: String,
    },

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

    .team_card{
        width: calc(100% / 4);
        position: relative;
        &:hover{

          .photo{
            display: none;
          }

          .info_user{
            display: block;
          }

        }

        img{
          width: 100%;

          &.photo{
            display: block;
          }
        }

        .info_user{
          display: none;
          background-image: url(../../assets/img/background-hover-dotted.jpeg);
          background-size: cover;
          height: 100%;

          .wrapper{
            width: 80%;
            height: 300px;
            background-color: $dark_red;
            margin: 0 auto;
            position: relative;
            top: 40px;

            .name{
              padding-top: 100px;
            }

            .role{
              font-weight: 300;
              font-family: sans-serif;
              padding-bottom: 10px;
            }
          }
            
        }
      }

</style>