<template>
  <div>
    <img :src="imgUrl" alt="">
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
    img{
        width: 100%;
        margin: 8px 0;
    }
</style>