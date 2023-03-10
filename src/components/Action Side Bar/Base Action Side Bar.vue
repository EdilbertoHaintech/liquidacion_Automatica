<template>
    <!-- Header -->
    <div class="row align-items-start justify-content-evenly">
        <button @click="changeTab('Validation')">
            <!-- <img src="assets/Check_Gray.png" alt="Validaciones" class="tabs_img" v-bind:class="{ 'active_tabs_img': botonClickeado }"> -->
            <img src="assets/Check_Basic.svg" alt="Validaciones" class="tabs_img active_tabs_img">
        </button>
        <button @click="changeTab('Medicines')">
            <img src="assets/Meds.svg" alt="Medicamentos" class="gray_filter">
        </button>
        <button @click="changeTab('Data')">
            <img src="assets/Data.svg" alt="Datos" class="gray_filter">
        </button>
        <button @click="changeTab('Bioequivalence')">
            <img src="assets/Chemistry.svg" alt="Bioequivalencia" class="gray_filter">
        </button>
    </div>
    <!-- Content -->
    <div class="content">
        <component :is="moduleSelected"></component>
    </div>
</template>

<script lang="ts">
import Validation from './Validation.vue';
import Medicines from './Medicines.vue';
import Data from './Data.vue';
import Bioequivalence from './Bioequivalence.vue';
import { DefineComponent } from 'vue';

export default {
    components: {
        Validation,
        Medicines,
        Data,
        Bioequivalence
    },
    methods: {
        changeTab(param: any) {
            this.moduleSelected = param;
            this.botonClickeado = true;
        }
    },
    data() {
        return {
            moduleSelected: "Medicines",
            botonClickeado: false
        }
    },
};
</script>

<style>
.tabs_img {
    height: 23px;
}

.active_tabs_img {
    padding: 0 0 5px 0;
    border-bottom: 2px solid var(--primary-color);
    border-radius: 2px;
    /* Filter to change color to Primary Color #E7632F on SVG*/
    /* Use https://codepen.io/sosuke/pen/Pjoqqp to get wanted color on SVG*/
    filter: invert(44%) sepia(62%) saturate(991%) hue-rotate(339deg) brightness(95%) contrast(90%);
}

.content {
    padding: 5px 10px 10px 10px;
    height: 72vh;
}
</style>