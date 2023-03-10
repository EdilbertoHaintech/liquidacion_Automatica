
import Validation from './Validation.vue';

<template>
    <!-- Header -->
    <div class="row align-items-start justify-content-evenly">
        <button>
            <img src="../../assets/Check_Orange.png" alt="Validaciones" class="tabs_img active_tabs_img">
        </button>
        <button>
            <img src="../../assets/Meds_Gray.png" alt="Medicamentos" class="tabs_img">
        </button>
        <button>
            <img src="../../assets/Data_Gray.png" alt="Datos" class="tabs_img">
        </button>
        <button>
            <img src="../../assets/Chemistry_Gray.png" alt="Bioequivalencia" class="tabs_img">
        </button>
    </div>
    <!-- Content -->
    <div class="content">
        <Validation></Validation>
        <Medicines></Medicines>
        <Data></Data>
        <Bioequivalence></Bioequivalence>
    </div>
</template>

<script lang="ts">
import Validation from './Validation.vue';
import Medicines from './Medicines.vue';
import Data from './Data.vue';
import Bioequivalence from './Bioequivalence.vue';

export default {
    components: {
        Validation,
        Medicines,
        Data,
        Bioequivalence
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
}

.content {
    padding: 10px;
    height: 72vh;
}
</style>