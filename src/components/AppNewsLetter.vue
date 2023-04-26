<script>
export default {
    name: "AppNewsletter",

};
</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->


<template>
    <div class="newsletter my-5">
        <div class="container simone d-flex flex-wrap justify-content-center gap-3">
            <div class="logo">
                <img class="label" src="../assets/img/7maggio.png">
                <img src="../assets/img/img/h-2-blog-img-1.jpg" alt="">
                <p class="my-3">This way,loves : a detailed guide trhought new deisgn</p>
                <p>by Emily Fields</p>
            </div>
            <div class="logo">
                <img class="label" src="../assets/img/7maggio.png">
                <img src="../assets/img/img/h-2-blog-img-2.jpg" alt="">
                <p class="my-3">I Try to give people a different way of looking art</p>
                <p>by Emily Fields</p>

            </div>
            <div class="logo">
                <img class="label" src="../assets/img/7maggio.png">
                <img src="../assets/img/img/h-2-blog-img-3.jpg" alt="">
                <p class="my-3">Introduce Richard Laperriere of those amazing features</p>
                <p>by Emily Fields</p>

            </div>
        </div>
    </div>
</template>

  
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
.simone {
    width: 100%;

    .logo {
        width: calc(100% / 3 - 30px);
        position: relative;

        .label {
            width: 30px;
            position: absolute;
            top: -10px;
            left: 10px;
        }
       
    }
}
</style>