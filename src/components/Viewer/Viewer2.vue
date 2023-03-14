<template>
    <div>
        <div v-if="isPDF">El archivo es un PDF</div>
        <div v-else-if="isImage">El archivo es una imagen</div>
        <div v-else>El archivo no es un PDF ni una imagen</div>
    </div>
</template>

<script lang="ts">
export default {
    data() {
        return {
            source: 'Example Tickets/boleta2.jpg', // Asignar la ruta del archivo aquí
        }
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