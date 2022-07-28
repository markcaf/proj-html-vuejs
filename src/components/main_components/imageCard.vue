<template>
  <div class="wrapper">
    <img :src="imgUrl" alt="">
    <div class="icon_hover text-center">
      <i class="fa-regular fa-eye"></i>
    </div>
  </div>
</template>

<script>
export default {
    name: 'imageCard',

    props: {
        imgUrl: String,
    },

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

  .wrapper{
    position: relative;
    transition: 0.5s ease-in-out; 

    &:hover{
      transform: scale(0.9);
      transition: transform 0.7s;
      background-image: url(../../assets/img/background-hover-dotted.jpeg);
      background-size: contain;

      img{
        opacity: 0;
        position: relative;
      }

      .icon_hover{
        display: block;
      }
    }

    img{
        width: 100%;
        margin: 8px 0;
    }

    .icon_hover{
      position: absolute;
      top: 40%;
      left: 42%;
      display: none;
      
      .fa-eye{
      font-size: 30px;
      padding: 10px;
      border-radius: 50%;
      background-color: $red_bg;
      color: white;
      }
    }
  }
</style>