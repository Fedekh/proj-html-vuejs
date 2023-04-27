<script>
export default {
    name: "NavBarHeader",
    props: {
        listMenu: Array
    },
    data() {
        return {
            currentMenuItem: null           //voci del menu nell header
        }
    },
    methods: {
        setMenuItem(item) {                 //voci del menu nell header
            this.currentMenuItem = item;
        }
    }
}

</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
    <ul class="d-sm-flex flex-md-row gap-3 m-0">
        <li v-for="(listitem, index) in listMenu" :key="index" :class="{ 'active': currentMenuItem === listitem }"
            @click="setMenuItem(listitem)">
            <a href="#">{{ listitem }}</a>
        </li>
        <a href=""><img class="align-self-center" src="../assets/svg/svg-1.svg" alt=""></a>
    </ul>
</template>
    
<!-- In questo modo, quando viene cliccato un elemento del menu, VueJS aggiungerà la classe active a quell'elemento
, attivando la regola CSS &.active:after, che applicherà la sottolineatura verde all'elemento cliccato.
 Allo stesso tempo, VueJS rimuoverà la classe active dall'elemento precedente, rimuovendo la sottolineatura verde -->

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/variables.scss" as *;
ul {
    li {
        font-weight: 600;
        position: relative;

        &:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background-color:$btn-border;
            transform: scaleX(0);
            transition: transform 0.3s ease-out;
            transform-origin: center;
        }

        &.active:after {
            transform: scaleX(1);
        }
    }

    img {
        width: 15px;
        height: 15px;
    }
}
</style>
