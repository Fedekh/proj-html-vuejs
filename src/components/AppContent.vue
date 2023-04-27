<script>
export default {
    name: "AppContent",
    data() {
        return {
            contentArray: [
                "../assets/img/img/h-2-port-img-1.jpg",
                "../assets/img/img/h-2-port-img-2.jpg",
                "../assets/img/img/h-2-port-img-3.jpg",
                "../assets/img/img/h-2-port-img-4.jpg",
                "../assets/img/img/h-2-port-img-5.jpg",
                "../assets/img/img/h-2-port-img-6.jpg"
            ]
        }
    },
    methods: {
        getImagePath(index) {
            return new URL(this.contentArray[index], import.meta.url).href;
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
            <div class="cont" v-for="(content, index) in contentArray" :key="index">
                <img :src="getImagePath(index)" alt="">
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
    border: 1px solid blue;
    .wrapper{
        width: 100%;
        .cont{
            width:calc(100% / 3);
        }
    }
    .shopper{
        // bottom: 600px;
        .shop{
            right: 20px;
            display: block;
            position: fixed;
            width: 30px;
            border: 1px solid none;
            z-index: 10;
        }
        .link1{
            background-color: red;
            top: 480px;
            img{
                margin: 5px;
            }
        }
        .link2{
            top: 550px;
            background-color: white;
            img{
                margin: 5px;
            }   
        }
    }
}
</style>