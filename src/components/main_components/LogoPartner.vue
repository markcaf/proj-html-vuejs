<template>
    <div class="logo_partner text-center">
        <img :src="imgUrl" alt="logo partner">
    </div>
</template>

<script>
export default {
    name: 'LogoPartner',

    props: {
        imgUrl: String,
    }

}
</script>

<style lang="scss" scoped>
    .logo_partner{
        width: 180px;
        img{
            width: 100%;
        }
    }

</style>