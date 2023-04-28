<script>
export default {
    name: "FooterList",
    props: {
        footerMenu: Object,
        stayInTouchIcons: Array
    },
};
</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->


<template>
    <li class="d-flex flex-column">
        <a href="">{{ footerMenu.email_phone[0] }}</a>
        <a href="">{{ footerMenu.email_phone[1] }}</a>

    </li>
    <li class="d-flex flex-column">
        <a href="">{{ footerMenu.address[0] }}</a>
        <a href="">{{ footerMenu.address[1] }}</a>
    </li>
    <li class="d-flex flex-column">
        <a href="">{{ footerMenu.stayInTouch[0] }}</a>
        <div>
            <a href="" class="mx-2" v-for="icon in stayInTouchIcons" :key="icon" v-html="icon"></a>
        </div>
    </li>
</template>


<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->


<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/variables.scss" as *;

@media (max-width: $md) {
    li {
        font-size: .6rem;
        margin: 10px;
        
        a{
            margin: 5px;
        }
    }
}
</style>
  
  