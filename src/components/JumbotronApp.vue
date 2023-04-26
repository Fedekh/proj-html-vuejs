<script >
export default {
    name: 'Jumbotron',
}

</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->


<template>
    <div class="wrapper">
        <section class="container d-sm-flex justify-content-between">
            <article class="col-5 description-jumbo d-sm-flex flex-column justify-content-center">
                <h1>Devotion that never <span>ends</span></h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem in eaque facilis ab totam debitis itaque id, sed maxime incidunt. Labore, reprehenderit! Necessitatibus quis voluptatibus, vero numquam possimus voluptate reiciendis.</p>
                <button class="btn"><a href="">READ MORE</a></button>
            </article>
            <div class="slider col-4">
                <img src="../assets/img/img/h-2-slider-img-16.png" alt="">
            </div>
        </section>
        <div class="cla">
            <i class="fa-solid fa-circle-chevron-left left-i" style="color: #e1c0b0;"></i>
            <i class="fa-solid fa-circle-chevron-right right-i" style="color: #e1c0b0;"></i>
        </div>
    </div>
</template>


<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->


<style lang="scss">
@use "../style/general.scss" as *;
@use "../style/partials/variables.scss" as *;

.wrapper {
    position: relative;
    width: 100%;

    section {
        width: $width-ms1;
        border: 1px solid rgb(117, 216, 117);
        .btn{
            border: 1px solid $btn-border;
            width: 200px;
        }

    }

    .cla {
        cursor: pointer;

        .left-i {
            position: absolute;
            left: 10px;
            top: 50%;

        }

        .right-i {
            position: absolute;
            top: 50%;

            right: 10px;

        }
    }
}
</style>