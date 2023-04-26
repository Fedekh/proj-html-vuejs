<script>
import NavBarHeader from "./NavBarHeader.vue";
import JumbotronApp from "./JumbotronApp.vue";

import { store } from "../store";

export default {
    name:'AppHeader',
    components: {
        NavBarHeader,
        JumbotronApp
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
    <section id="header" class="wrap">
        <div class="container d-sm-flex justify-content-between align-items-center">
            <div class="logo"><img src="../assets/img/img/logo-sidearea-1.png" alt=""></div>
            <NavBarHeader :listMenu="navBarMenu"/>
        </div>
    </section>
    <div class="container">
        <JumbotronApp/>
    </div>
</template>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style scoped lang="scss">
@use "../style/partials/variables.scss" as *;
.wrap{
    border: 1px solid red;
    position: relative;
    .container{
        height: $header-h;
    }
    
}
</style>