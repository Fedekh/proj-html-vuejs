<script>
import FooterList from "./FooterList.vue";

export default {
    name: 'AppFooter',
    components: {
        FooterList,
    },
    data() {
        return {
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
    methods: {
        getImagePath() {
            return new URL(this.footerMenu.logo[0], import.meta.url).href;
        }
    }
}

</script>


<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
    <section id="footer" class="wrapper-footer">
        <div class="footer">
            <ul class="container d-flex flex-row justify-content-evenly align-items-center">
                <li class="text-center">
                    <a href="">
                        <img :src="getImagePath()" alt="">
                    </a>
                    <p>{{ footerMenu.logo[1] }}</p>
                </li>
                <FooterList :footerMenu="footerMenu" :stayInTouchIcons="footerMenu.stayInTouch[1]" />
            </ul>
        </div>

    </section>
</template>


<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/variables.scss" as *;

.wrapper-footer {
    position: relative;
    background-color: $footer-bg;

    .container {
        height: $footer-h;
        margin-bottom: 0;
        font-size: 0.7rem;

        @media (max-width: $md) {
            p {
                font-size: .5rem;
            }
        }
    }

}
</style>