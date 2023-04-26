<script>
import AppContent from "./AppContent.vue";
import AppFeatures from "./AppFeatures.vue";
import AppContacts from "./AppContacts.vue"
import AppNewsLetter from "./AppNewsLetter.vue";
import { store } from "../store";

export default {
    name: 'AppMain',
    components: {
        AppFeatures,
        AppContent,
        AppContacts,
        AppNewsLetter
    },
    data() {
        return {
            store
        }
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