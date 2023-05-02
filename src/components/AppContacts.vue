<script>
export default {
    name: "AppContacts"
}


</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
    <section>
        <div class="wrapper container d-flex flex-column justify-content-center align-items-center">
            <h2>Want to work with us ? Send us <span>a message!</span></h2>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ducimus eum harum, nihil quasi a quis impedit
                temporibus veniam eligendi, praesentium perspiciatis, atque velit numquam assumenda itaque qui officia.
                Quaerat, magnam.</p>
            <button class="btn"><a href="#header">CONTACT</a></button>
        </div>
    </section>
</template>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/partials/variables.scss" as *;

section {
    background-image: url('../assets/img/background-contact.jpg');
    background-size: cover;
    filter: opacity(.8);

    .wrapper {
        height: 500px;
        position: relative;

        button {
            border: none;
            background-color: $footer-bg;
            width: 150px;
            height: 40px;
            transition: .5s linear;

            &:hover {
                transform: scale(1.2);
                background-color: $footer-bg;

            }
        }

    }
}
</style>