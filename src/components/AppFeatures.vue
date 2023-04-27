<script>
export default {
    name: "AppFeatures",
}

</script>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
    <div class="feature">
        <div class="container my-5 d-flex flex-column justify-content-center align-items-center">
            <h2>Working <span>process</span></h2>
            <div class="cta text-center d-flex gap-5 my-5">
                <img class="wave" src="../assets/svg/svg-3.svg" alt="">
                <div class="d-flex flex-column align-items-center">
                    <div class="cta-image text-center">
                        <i class="fa-regular fa-lightbulb" style="color: #c0e1cf;"></i>
                    </div>
                    <h4>First theres an idea</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, dicta voluptates dolorem
                        doloribus ea tempora ab. .</p>
                </div>
                <div class="d-flex flex-column align-items-center">
                    <div class="cta-image">
                        <i class="fa-solid fa-cloud" style="color: #80465f;"></i>
                    </div>
                    <h4>Then we talk about</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, dicta voluptates dolorem
                        doloribus ea tempora ab. .</p>
                </div>
                <div class="d-flex flex-column align-items-center">
                    <div class="cta-image">
                        <i class="fa-regular fa-comment" style="color: #f8d33b;"></i>
                    </div>
                    <h4>And we think about</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, dicta voluptates dolorem
                        doloribus ea tempora ab. .</p>
                </div>
                <div class="d-flex flex-column align-items-center">
                    <div class="cta-image">
                        <i class="fa-solid fa-compass-drafting" style="color: #ec7963;"></i>
                    </div>
                    <h4>So we draw along</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, dicta voluptates dolorem
                        doloribus ea tempora ab. .</p>
                </div>
            </div>
        </div>
    </div>
</template>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/variables.scss" as *;

.feature {
    position: relative;

    h2 {
        font-size: 3rem;
    }

    .cta {
        position: relative;

        .wave {
            position: absolute;
            left: 124px;
            top: -6px;
            z-index: -1;
            width: 76%;
        }
    }

    .cta-image {
        margin-bottom: 30px;
        position: relative;
        border-radius: 50%;
        width: 100px;
        height: 100px;
        background-color: #FAF7F1;

        i {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 2rem;
        }


    }
}
</style>