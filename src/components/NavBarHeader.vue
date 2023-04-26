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
<ul class="d-sm-flex flex-md-row gap-3">
   <li v-for="(listitem,index) in listMenu" :key="index"> <a href="#">{{ listitem }}</a></li>
   <i class="align-self-center fa-solid fa-border-none"></i>
</ul>
</template>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
</style>