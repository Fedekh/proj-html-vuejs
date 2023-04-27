<script>
export default {
    name: "AppContent",
    data() {
        return {
            contents: [
                {
                    imagePath: "../assets/img/img/h-2-port-img-1.jpg",
                    info: "Frederich Einstein",
                    sub: "GOAT",

                },
                {
                    imagePath: "../assets/img/img/h-2-port-img-2.jpg",
                    info: "Tandem additced",
                    sub: "Couple",
                },
                {
                    imagePath: "../assets/img/img/h-2-port-img-3.jpg",
                    info: "The lord of the rings",
                    sub: "Sauron defeated",

                },
                {
                    imagePath: "../assets/img/img/h-2-port-img-4.jpg",
                    info: "Illustrations of novels",
                    sub: "Illustration",

                },
                {
                    imagePath: "../assets/img/img/h-2-port-img-5.jpg",
                    info: "The new Smartphone",
                    sub: "Oneplus rulez",

                },
                {
                    imagePath: "../assets/img/img/h-2-port-img-6.jpg",
                    info: "Listen music",
                    sub: "Relax",

                }
            ]

        }
    },
    methods: {
        getImagePath(index) {
            return new URL(this.contents[index].imagePath, import.meta.url).href;
        }

    }
}

</script>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
    <div class="content">
        <div class="shopper">
            <a class="my-3 shop link1" href=""><img src="../assets/svg/svg-4.svg" alt=""></a>
            <a class="my-3 shop link2" href=""><img src="../assets/svg/svg-6.svg" alt=""></a>
        </div>
        <div class="wrapper d-flex flex-wrap">
            <div class="cont" v-for="(content, index) in contents" :key="index">
                <img :src="getImagePath(index)" alt="">
                <div class="overlay">
                    <p>{{ content.info }}</p>
                    <p class="sub">{{ content.sub }}</p>

                </div>
            </div>
        </div>

    </div>
</template>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/variables.scss" as *;

.content {
    position: relative;
    .wrapper {
        width: 100%;
        position: relative;

        .cont {
            width: calc(100% / 3);
            position: relative;

            &:hover .overlay {
                display: block;
                position: absolute;
                top: 70px;
                left: 10px;
                transform: translateY(-50%);
                z-index: 3;
                background-color: rgba(0, 128, 0, 0.4);
                color: #fff;
                padding: 20px;
                border-radius: 10px;
                box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
                transition: all 2s ease-in-out;
                transition: background-color 2s ease-in-out;
                clip-path: polygon(0 0, 100% 0, 100% 80%, 50% 100%, 0 80%);
            }

            .overlay {
                display: none;
            }

            .sub {
                font-style: italic;
            }

        }
    }

    .shopper {

        // bottom: 600px;
        .shop {
            right: 20px;
            display: block;
            position: fixed;
            width: 30px;
            border: 1px solid none;
            z-index: 10;
        }

        .link1 {
            background-color: red;
            top: 570px;

            img {
                margin: 5px;
            }
        }

        .link2 {
            top: 620px;
            background-color: white;

            img {
                margin: 5px;
            }
        }
    }
}
</style>