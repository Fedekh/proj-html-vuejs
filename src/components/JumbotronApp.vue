<script >
export default {
    name: 'Jumbotron',
    data() {
        return {
            sliders: [
                "../assets/img/img/h-2-slider-img-11.png",
                "../assets/img/img/h-2-slider-img-15.png",
                "../assets/img/img/h-2-slider-img-16.png"
            ],
            activeImage: 0,                 // indice immagine dinamico
            sensoMarcia: false,          //flag senso di marcia
            time: 3000                   // intervallo dell'autoplay carosello
        }
    },
    methods: {
        getImagePath(activeImage) {
            return new URL(this.sliders[activeImage], import.meta.url).href;
        },

        showNext() {
            clearInterval(this.interval);
            if (this.activeImage < this.sliders.length - 1) {
                this.activeImage++;
            } else {
                this.activeImage = 0;
            }
            this.sensoMarcia = false;
            this.startAutoplay();
        },

        showPrev() {
            clearInterval(this.interval);
            if (this.activeImage > 0) {
                this.activeImage--;
            } else {
                this.activeImage = this.sliders.length - 1;
            }
            this.sensoMarcia = true;
            this.startAutoplay();
        },

        startAutoplay() {
            this.interval = setInterval(() => {
                if (this.sensoMarcia) {
                    this.showPrev();
                } else {
                    this.showNext();
                }
            }, this.time);
        },

        showslide(indexToShow) {
            this.activeImage = indexToShow;
        },

        mouseHover() {
            clearInterval(this.interval);
        },

        mouseLeave() {
            this.startAutoplay();
        }
    },
    mounted() {
        this.startAutoplay();

    }
}

</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->


<template>
    <div class="wrapper pt-1 pb-5 my-5">
        <section class="container d-sm-flex justify-content-between">
            <article class="col-5 description-jumbo d-sm-flex flex-column justify-content-center">
                <h1>Devotion that never <span>ends</span></h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem in eaque facilis ab totam debitis itaque
                    id, sed maxime incidunt. Labore, reprehenderit! Necessitatibus quis voluptatibus, vero numquam possimus
                    voluptate reiciendis.</p>
                <button class="btn"><a href="">READ MORE</a></button>
            </article>
            <div class="slider col-4 align-self-center" @mouseover="mouseHover" @mouseleave="mouseLeave">
                <div>
                    <div class="slider-image">
                        <img id="slider-image" :src="getImagePath(activeImage)" alt="" />
                    </div>
                </div>
            </div>
        </section>
        <div class="cla">
            <i @click="showPrev" class="fa-solid fa-circle-chevron-left left-i"></i>
            <i @click="showNext" class="fa-solid fa-circle-chevron-right right-i"></i>
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
        height: 350px;
        border: 1px solid rgb(117, 216, 117);

        .btn {
            border: 1px solid $btn-border;
            width: 200px;
        }
        #slider-image{
            width: 300px;
        }
    }


    .cla {
        cursor: pointer;
        color: $btn-border;
        font-size: 2rem;

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