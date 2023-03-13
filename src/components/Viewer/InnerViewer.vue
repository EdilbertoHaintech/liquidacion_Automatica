<template>
    <div class="viewerContainer">
        <vue-pdf-embed :source="source1" />
        <!-- <vue-image-zoomer regular="path-to-regular.jpg" zoom="path-to-zoom.jpg" /> -->
    </div>
</template>

<script lang="ts">
import VuePdfEmbed from 'vue-pdf-embed';
// import { VueImageZoomer } from 'vue-image-zoomer'
// import 'vue-image-zoomer/dist/style.css';

// OR THE FOLLOWING IMPORT FOR VUE 2
// import VuePdfEmbed from 'vue-pdf-embed/dist/vue2-pdf-embed'

export default {
    components: {
        VuePdfEmbed,
        // VueImageZoomer
    },
    data() {
        return {
            source1: 'Example Tickets/boleta.pdf',
            source2: 'data:application/pdf;base64,<BASE64_ENCODED_PDF>',
        }
    },
}
</script>

<style></style>