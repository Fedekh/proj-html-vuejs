<script>
export default {
    name:"NavBarHeader",
    props:{
        listMenu:Array
    },
}

</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
<ul class="d-sm-flex flex-md-row gap-3 m-0">
   <li v-for="(listitem,index) in listMenu" :key="index"> <a href="#">{{ listitem }}</a></li>
   <a href=""><img class="align-self-center" src="../assets/svg/svg-1.svg" alt=""></a>
</ul>
</template>


<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>

ul{
    img{
        width: 15px;
        height: 15px;
    }
}
</style>