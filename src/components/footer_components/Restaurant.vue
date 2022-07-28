<template>
    <li>
        <div class="address">{{address}}</div>
        <div class="city">{{city}}</div>
        <div class="tel">{{tel}}</div>
    </li>
</template>

<script>
export default {
    name: 'Restaurant',

    props: {
        address: String,
        city: String,
        tel: String,
    }

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

    li{
        color: $p_secondary;
        font-family: sans-serif;
        margin: 20px 0;
    }

</style>