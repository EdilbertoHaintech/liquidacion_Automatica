<template>
    <div>
        <vue-pdf-embed :source="source1" />
    </div>
</template>

<script lang="ts">
import VuePdfEmbed from 'vue-pdf-embed'

// OR THE FOLLOWING IMPORT FOR VUE 2
// import VuePdfEmbed from 'vue-pdf-embed/dist/vue2-pdf-embed'

export default {
    components: {
        VuePdfEmbed,
    },
    data() {
        return {
            source1: 'assets/Vue-3-Cheat-Sheet.pdf',
            source2: 'data:application/pdf;base64,<BASE64_ENCODED_PDF>',
        }
    },
}
</script>