<template>
    <div class="viewerContainer">
        <!-- PDF -->
        <div v-if="isPDF">
            <vue-pdf-embed ref="pdfEmbed" :source="source" :height="700" :scale="scale" />
            <!-- <vue-pdf-embed ref="pdfEmbed" :source="source1"  :height="700"/> -->
        </div>
        <div v-else-if="isImage">
            <img :src="source" :height="700" alt="Imagen">
        </div>
        <div v-else>
            El archivo no es un PDF ni una imagen
        </div>

        <!-- Rotate, Zoom a Restart buttons to manipulate the image -->
        <div class="imageControls">
            <button type="button">
                <img src="assets/refresh.svg" alt="Restablecer">
            </button>
            <button type="button">
                <img src="assets/Undo_Arrow3.svg" alt="Rotar Izquierda">
            </button>
            <button type="button">
                <img src="assets/Undo_Arrow4.svg" alt="Rotar Derecha">
            </button>
            <!-- <button type="button" @click="zoom(0.1)"> -->
            <button type="button">
                <img src="assets/zoom-in.svg" alt="Zoom In">
            </button>
            <button type="button">
                <img src="assets/zoom-out.svg" alt="Zoom Out">
            </button>
        </div>
        <!-- <vue-image-zoomer regular="path-to-regular.jpg" zoom="path-to-zoom.jpg" /> -->
    </div>
</template>

<script lang="ts">
import VuePdfEmbed from 'vue-pdf-embed';
// import { VueImageZoomer } from 'vue-image-zoomer'
// import 'vue-image-zoomer/dist/style.css';

export default {
    components: {
        VuePdfEmbed,
        // VueImageZoomer
    },
    data() {
        return {
            // PDF 'Example Tickets/boleta.pdf',
            // JPG 'Example Tickets/boleta2.jpg',
            source: 'Example Tickets/boleta.pdf',
            // source2: 'data:application/pdf;base64,<BASE64_ENCODED_PDF>',
            scale: 2.0,
        };
    },
    methods: {
        // zoom(valor: any) {
        //     this.scale += valor;
        //     console.log(this.$refs.pdfEmbed);
        //     this.$refs.pdfEmbed.setScale(this.scale);
        // }
    },
    computed: {
        isPDF() {
            return this.source.toLowerCase().endsWith('.pdf')
        },
        isImage() {
            const imageExtensions = ['.png', '.jpg', '.jpeg', '.gif', '.bmp']
            const extension = this.source.toLowerCase().substr(this.source.lastIndexOf('.'))
            return imageExtensions.includes(extension)
        },
    },
}
</script>

<style>
.viewerContainer {
    height: 100%;
    width: 100%;
    position: relative;
}

.imageControls {
    position: absolute;
    bottom: 0;
    right: 0;
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    align-items: flex-end;
    justify-content: flex-end;
    padding: 10px;
}
</style>