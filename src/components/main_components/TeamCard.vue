<template>
  <div class="team_card">
    <img :src="imgUrl" alt="">
  </div>
</template>

<script>
export default {
    name: 'TeamCard',

    props: {
      id: String,
      imgUrl: String,
    },

}
</script>

<style lang="scss" scoped>
    .team_card{
        width: calc(100% / 4);
        img{
            width: 100%;
        }
    }

</style>