<template>
    <!-- Header -->
    <div class="row align-items-start justify-content-evenly">
        <button v-for="button in buttons" @click="changeTab(button.component)">
            <img :src="button.image" :alt="button.component" class="tabs_img gray_filter"
                :class="{ 'active_tabs_img': moduleSelected == button.component }">
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
        changeTab(param: string): void {
            this.moduleSelected = param;
            this.botonClickeado = true;
        }
    },
    data() {
        return {
            buttons: [
                {
                    component: 'Validation',
                    image: 'assets/Check_Basic.svg',
                },
                {
                    component: 'Medicines',
                    image: 'assets/Meds.svg',
                },
                {
                    component: 'Data',
                    image: 'assets/Data.svg',
                },
                {
                    component: 'Bioequivalence',
                    image: 'assets/Chemistry.svg',
                }
            ],
            moduleSelected: "Validation",
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
    padding: 5px 0 10px 10px;
    height: 650px;
}
</style>