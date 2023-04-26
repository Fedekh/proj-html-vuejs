<script>
import NavBar from "./NavBar.vue";
import JumbotronApp from "./JumbotronApp.vue";

import { store } from "../store";

export default {
    name:'AppHeader',
    components: {
        NavBar,
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
    <section id="header" class="wrapper">
        <div class="container d-sm-flex justify-content-between align-items-center">
            <div class="logo"><img src="../assets/img/img/logo-sidearea-1.png" alt=""></div>
            <NavBar :listMenu="navBarMenu"/>
        </div>
    </section>
    <div class="container">
        <JumbotronApp/>
    </div>
</template>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style scoped lang="scss">
@use "../style/partials/variables.scss" as *;
.wrapper{
    border: 1px solid red;
    position: relative;
    
}
</style>