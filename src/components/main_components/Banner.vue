<template>
  <div class="banner d-flex align-items-center justify-content-center mb-2">
    <div class="content text-uppercase text-white">
        Go ahead and<br> build your<br> own pizza<br> we won't<br> judge!
    </div>
  </div>
</template>

<script>
export default {
    name: 'Banner',

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
    .banner{
        height: 600px;
        background-image: url(../../assets/img/h3-background-img.jpg);
        background-size: cover;
        background-position: top;

        .content{
            font-size: 70px;
            font-weight: 500;
            line-height: 75px;
            margin-right: 35%;
        }

    }

</style>