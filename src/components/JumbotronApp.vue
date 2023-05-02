<script >
export default {
    name: 'Jumbotron',
    data() {
        return {
            outLineImg: [                                           // array di immagini di abbellimento (le maledette foglioline)
                "../assets/img/img/h-2-slider-img-12.png",
                "../assets/img/img/h-2-slider-img-13.png",
                "../assets/img/img/h-2-slider-img-14.png",
                "../assets/img/img/h-2-slider-img-17.png",
                "../assets/img/img/short-slider-rev-1-img-2.png",
                "../assets/img/img/short-slider-rev-1-img-6.png"
            ],
            sliders: [                                              // array di immagini del carosello
                "../assets/img/img/h-2-slider-img-11.png",
                "../assets/img/img/h-2-slider-img-15.png",
                "../assets/img/img/h-2-slider-img-16.png"
            ],
            activeImage: 0,                 // indice immagine dinamico
            interval: null,                //mi servirà settato vuoto per far partire l'autoplay al refresh di pagina
            sensoMarcia: false,          //flag senso di marcia
            time: 3000                   // intervallo dell'autoplay carosello
        }
    },
    methods: {
        getImagePath(activeImage) {                                     // funzione per prendere il path dell'immagine
            return new URL(this.sliders[activeImage], import.meta.url).href;
        },
        getOutLineImgPath(index) {                                      // funzione per prendere il path delle foglioline
            return new URL(this.outLineImg[index], import.meta.url).href;
        },

        showNext() {                                    // funzione per mostrare l'immagine successiva
            clearInterval(this.interval);
            if (this.activeImage < this.sliders.length - 1) {
                this.activeImage++;
            } else {
                this.activeImage = 0;
            }
            this.sensoMarcia = false;
            this.startAutoplay();
        },
        showPrev() {                                    // funzione per mostrare l'immagine precedente
            clearInterval(this.interval);
            if (this.activeImage > 0) {
                this.activeImage--;
            } else {
                this.activeImage = this.sliders.length - 1;
            }
            this.sensoMarcia = true;
            this.startAutoplay();
        },
        startAutoplay() {                                   // funzione per l'autoplay
            this.interval = setInterval(() => {
                if (this.sensoMarcia) {
                    this.showPrev();
                } else {
                    this.showNext();
                }
            }, this.time);
        },
        mouseHover() {                              // funzione per fermare l'autoplay al mousehover
            clearInterval(this.interval);
        },

        mouseLeave() {                          // funzione per far ripartire l'autoplay dopo il mouseleave
            this.startAutoplay();
        },
        showslide(indexToShow) {                // funzione per mostrare l'immagine cliccata nei dots piccoli
            clearInterval(this.interval);
            this.activeImage = indexToShow;
            this.startAutoplay();
        }
    },
    mounted() {                           // funzione per far partire l'autoplay all'apertura della pagina
        this.startAutoplay();

    }
}

</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->


<template>
    <div class="wrapper pt-1 pb-5 my-5">
        <section class="container d-sm-flex justify-content-between">
            <article class="col-5 description-jumbo d-sm-flex flex-column justify-content-center">
                <h1 class="text-center rounded p-2">Devotion that never <span>ends</span></h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem in eaque facilis ab totam debitis itaque
                    id, sed maxime incidunt. Labore, reprehenderit! Necessitatibus quis voluptatibus, vero numquam possimus
                    voluptate reiciendis.</p>
                <button class="btn mx-auto"><a href="">READ MORE</a></button>
            </article>
            <div class="outline">
                <div v-for="(element, index) in outLineImg" :id="`out_${index + 1}`"><img :src="getOutLineImgPath(index)"
                        alt=""></div>
            </div>
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
        <div class="slider-dots">
            <i v-for="i in sliders.length" :key="i" :class="['fas', 'fa-circle', { active: activeImage === i - 1 }]"
                @click="showslide(i - 1)"></i>
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

        article {
            h1 {
                background-color: yellow;
            }

            p {
                font-size: 1rem;
            }

            .btn {
                border: 1px solid $btn-border;
                width: 200px;
                font-weight: bold;


                &:hover {
                    background-color: $btn-border;
                    transition: 1s linear;
                }
            }

            @media (max-width: $md) {
                h1 {
                    font-size: 1.5rem;
                }

                p {
                    font-size: .7rem;
                }

                .btn {
                    font-size: .7rem;
                    width: 100px;
                }
            }

        }

        .outline {
            div {
                position: absolute;
                width: 40px;
            }

            #out_1 {
                bottom: 45%;
                right: 50%;
            }

            #out_2 {
                bottom: 20%;
                left: 55%;
            }

            #out_3 {
                top: 0%;
                right: 6%;
            }

            #out_4 {
                bottom: 20%;
                right: 2%;
            }

            #out_5 {
                right: 42%;
            }

            #out_6 {
                top: 24%;
                right: 3%;
            }
        }

        .slider {

            .slider-image {
                cursor: pointer;
                scale: 1;
                transition: all .5s ease-in-out;

                &:hover {
                    scale: 1.4;
                    transition: all .5s ease-in-out;
                }

                #slider-image {
                    width: 300px;
                }
            }
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

    .slider-dots {
        position: absolute;
        left: 50%;

        i {
            margin: 0 5px;
            cursor: pointer;
            margin-inline: 10px;
            font-size: .6rem;
            color: $btn-border;

            &.active {
                font-size: 1rem;
                transform: scale(1.5);
            }
        }

    }
}
</style>