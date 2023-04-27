<script>
import NavBarHeader from "./NavBarHeader.vue";
import JumbotronApp from "./JumbotronApp.vue";

import { store } from "../store";

export default {
    name: 'AppHeader',
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
        <div class="ms_container1 d-sm-flex justify-content-between align-items-center">
            <a href=""><img src="../assets/img/img/logo-sidearea-1.png" alt=""></a>
            <NavBarHeader :listMenu="navBarMenu" />
        </div>
    </section>
    <div class="ms_container1">
        <JumbotronApp />
    </div>
</template>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style scoped lang="scss">
@use "../style/general.scss" as *;
@use "../style/partials/variables.scss" as *;

.wrap {
    position: relative;
    .ms_container1{
        height: $header-h;
     
        .jumbo-container {
            position: relative;
    
        }
    }

}
</style>