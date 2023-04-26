<script>
import AppNavBar from "./AppNavBar.vue";

import { store } from "../store";

export default {
    name:'AppHeader',
    components: {
        AppNavBar
    },
    data() {
        return {
            store,
            navBarMenu: ["HOME", "PAGES", "PORTFOLIO", "BLOG", "SHOP", "ELEMENTS"]        //voci del menu nell header

        }
    }
}

</script>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
    <div class="wrapper">
        <div class="logo"><img src="../assets/img/img/logo-sidearea-1.png" alt=""></div>
        <AppNavBar :listMenu="navBarMenu"/>
    </div>
</template>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/general.scss";
</style>