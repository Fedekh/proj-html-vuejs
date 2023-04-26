<script>
// import { store } from "../store";

export default {
    name:"AppNavBar",
    props:{
        listMenu:Array,
    },
}

</script>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
<ul class="d-xs-flex flex-md-row ">
    <li v-for="(listitem,index) in listMenu" :key="index"> {{ listitem }}</li>
</ul>
</template>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/general.scss";
</style>