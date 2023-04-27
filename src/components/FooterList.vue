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
    <li>
        <p>{{ footerMenu.email_phone[0] }}</p>
        <p>{{ footerMenu.email_phone[1] }}</p>
    </li>
    <li>
        <p>{{ footerMenu.address[0] }}</p>
        <p>{{ footerMenu.address[1] }}</p>
    </li>
    <li>
        <p>{{ footerMenu.stayInTouch[0] }}</p>
        <div>
            <a href="" class="mx-2" v-for="icon in stayInTouchIcons" :key="icon" v-html="icon"></a>
        </div>
    </li>
</template>


<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->


<style lang="scss" scoped>
</style>
  
  