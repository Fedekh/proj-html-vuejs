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
            navBarMenu: ["HOME", "PAGES", "PORTFOLIO", "BLOG", "SHOP", "ELEMENTS"],        //voci del menu nell header
            metaColorScheme: null,
            themeSwitch: null,
            darkMode: false,
            store

        }
    }}

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
    box-shadow: 15px 9px 15px 13px rgb(0 0 0 / 0.8);

    input[type="checkbox"] {
        position: relative;
        width: 80px;
        height: 40px;
        -webkit-appearance: none;
        appearance: none;
        background: #fff;
        outline: none;
        border-radius: 2rem;
        cursor: pointer;
        box-shadow: inset 0 0 5px rgb(0 0 0 / 50%);
    }

    input[type="checkbox"]::before {
        content: "";
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background: red;
        background: #00ed64;
        position: absolute;
        top: 0;
        left: 0;
        transition: 0.5s;
    }

    input[type="checkbox"]:checked::before {
        transform: translateX(100%);
        background: #00ed64;

    }

    input[type="checkbox"]:checked {
        background: black;
    }

    .ms_container1 {
        height: $header-h;

        .jumbo-container {
            position: relative;
        }
    }
}
</style>