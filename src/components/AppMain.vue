<script>
import AppContent from "./AppContent.vue";
import AppFeatures from "./AppFeatures.vue";
import AppContacts from "./AppContacts.vue"
import AppNewsLetter from "./AppNewsLetter.vue";

export default {
    name: 'AppMain',
    components: {
        AppFeatures,
        AppContent,
        AppContacts,
        AppNewsLetter
    }
}

</script>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
    <AppContent />
    <AppFeatures />
    <AppContacts />
    <AppNewsLetter />
</template>
<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
// @use "../style/general.scss";
</style>