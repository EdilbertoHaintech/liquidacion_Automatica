<template>
    <div class="d-flex flex-column">
        <span class="title_section">Bioequivalencia</span>
        <ControlHeaderTable></ControlHeaderTable>
        <div v-for="(medicine, index) in medicineData" :key="index">
            <details>
                <summary>{{ medicine.nombre }}</summary>
                <ul>
                    <li v-for="(bioequivalente, i) in medicine.bioequivalentes" :key="i">{{ bioequivalente }}</li>
                </ul>
            </details>
        </div>
    </div>
</template>

<script lang="ts">
import ControlHeaderTable from './ControlHeaderTable.vue';
import BioquevalenceData from "../../../../public/JSON/Bioquevalence";

export default {
    components: {
        ControlHeaderTable
    },
    data() {
        return {
            medicineData: BioquevalenceData
        }
    }
};
</script>