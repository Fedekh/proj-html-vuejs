<script>
import NavBarHeader from "./NavBarHeader.vue";
import JumbotronApp from "./JumbotronApp.vue";


export default {
    name: 'AppHeader',
    components: {
        NavBarHeader,
        JumbotronApp
    },
    data() {
        return {
            navBarMenu: ["HOME", "PAGES", "PORTFOLIO", "BLOG", "SHOP", "ELEMENTS"]        //voci del menu nell header

        }
    }
}

</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
    <header id="header" class="wrap">
        <div class="ms_container1 d-flex justify-content-between align-items-center">
            <a href=""><img src="../assets/img/img/logo-sidearea-1.png" alt=""></a>
            <NavBarHeader :listMenu="navBarMenu" />
        </div>
    </header>
    <div class="ms_container1">
        <JumbotronApp />
    </div>
</template>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style scoped lang="scss">
@use "../style/partials/variables.scss" as *;

.wrap {
    position: relative;
    box-shadow:15px 9px 15px 13px rgb(0 0 0 / 0.8);
    .ms_container1{
        height: $header-h;
     
        .jumbo-container {
            position: relative;
        }
    }
}
</style>