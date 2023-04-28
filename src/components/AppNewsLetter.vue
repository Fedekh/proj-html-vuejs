<script>
export default {
    name: "AppNewsletter",
    data() {
        return {
            logos: [
                {
                    img: "../assets/img/img/h-2-blog-img-1.jpg",
                    descr: 'This way,loves : a detailed guide trhought new deisgn',
                    sub: 'by Emily Fields',
                    day: '07',
                    mounth_year: 'May 19'
                },
                {
                    img: "../assets/img/img/h-2-blog-img-2.jpg",
                    descr: 'I Try to give people a different way of looking art',
                    sub: 'by Emily Fields',
                    day: '07',
                    mounth_year: 'May 19'
                },
                {
                    img: "../assets/img/img/h-2-blog-img-3.jpg",
                    descr: 'Introduce Richard Laperriere of those amazing features',
                    sub: 'by Emily Fields',
                    day: '07',
                    mounth_year: 'May 19'
                }
            ]
        }
    },
    methods: {
        getImagePath(elemento) {
            return new URL(elemento.img, import.meta.url).href;
        }
    }

};
</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->


<template>
    <div class="newsletter">
        <a class="up d-flex justify-content-center" href="#header"><img src="../assets/svg/svg-2.svg" alt=""></a>
        <div
            class="container d-sm-flex flex-md-row flex-md-wrap justify-content-md-center gap-3 flex-xs-nowrap flex-sm-column align-items-sm-center">
            <div class="logo text-center" v-for="element, index in logos" :key="index">
                <div class="tag text-center">
                    <p class="day text-center">{{ element.day }}</p>
                    <p class="month mx-1">{{ element.mounth_year }}</p>
                </div>
                <img :src="getImagePath(element)" alt="">
                <div class="text px-2">
                    <p class="descr my-3">{{ element.descr }}</p>
                    <p class="sub">{{ element.sub }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

  
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/variables.scss" as *;

.newsletter {
    position: relative;
    padding: 90px 0;

    .logo {
        width: calc(100% / 3 - 30px);
        position: relative;
        cursor: pointer;
        filter: blur(1px);
        background-color: #fff;
        transition: all .8s ease-in-out;

        &:hover {
            filter: blur(0);
            background-color: #5fdf0a97;
            transform: scale(1.2);
            position: relative;
            top: -20px;
            z-index: 9;
            box-shadow: -1px 3px 20px 20px rgba(0, 0, 0, 0.7);
        }

        .tag {
            position: absolute;
            top: -40px;
            left: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .day {
            background-color: $footer-bg;
            color: black;
            font-size: 1.3rem;
            font-style: italic;
            width: 48px;
            clip-path: polygon(50% 10, 100% 50%, 50% 100%, 0 50%);
            margin-bottom: 0;
        }

        .month {
            background-color: #F4DBDA;
            color: #1c1c1c;
            font-size: 0.8rem;
            font-weight: bold;
            padding: 1rem;
            clip-path: polygon(9% 2%, 90% 2%, 90% 100%, 48% 78%, 9% 100%);
            margin-top: -2px;
            width: 60px;
        }

        .descr {
            font-weight: 600;

        }

        .sub {
            font-style: italic;
            font-weight: 500;
        }

        @media (max-width: $md) {
            p {
                font-size: .7rem;
            }
        }
    }

}
</style>