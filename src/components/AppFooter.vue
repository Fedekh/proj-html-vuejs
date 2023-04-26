<script>
import { store } from "../store";

export default {
    name: 'AppFooter',
    data() {
        return {
            store,
            footerMenu: {                   // footerMenu:object
                logo: ["../assets/img/img/logo-sidearea-1-1.png", "Let's get creative"],
                email_phone: ["pippo@gmail.com", "+35 68 44 88"],
                address: ["Avenue d'Augherdem 10", "1040 Brussel, Belgium"],
                stayInTouch: ["Stay in Touch with us",
                    [
                        '<i class="fab fa-twitter"></i>',
                        '<i class="fab fa-pinterest-p"></i>',
                        '<i class="fab fa-facebook-f"></i>',
                        '<i class="fa-brands fa-linkedin"></i>',
                    ]
                ]

            }

        }
    },
    methods:{
        getImagePath() {
            return new URL(this.footerMenu.logo[0], import.meta.url).href;
        }
    }
}

</script>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
    <section class="wrapper-footer">
        <div class="footer">
            <ul class="container d-flex justify-content-evenly align-items-center">
                <li class="text-center">
                    <a href="">
                        <img :src="getImagePath()" alt="">
                    </a>
                    <p>{{ footerMenu.logo[1] }}</p>
                </li>
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
                    <div class="">
                        <a href="" class="mx-2" v-for="icon in footerMenu.stayInTouch[1]" :key="icon" v-html="icon"></a>
                    </div>
                </li>
            </ul>
        </div>
    </section>
</template>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/partials/variables.scss" as *;

.wrapper-footer {
    background-color: $footer-bg;

    .container {
        height: $footer-h;
    }
}
</style>