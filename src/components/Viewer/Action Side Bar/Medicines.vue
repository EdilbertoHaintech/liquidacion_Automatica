<template>
    <div class="d-flex flex-column">
        <span class="title_section">Medicamentos</span>
        <ControlHeaderTable></ControlHeaderTable>
        <table>
            <thead>
                <tr>
                    <th><input type="checkbox" />R</th>
                    <th>Código</th>
                    <th>Medicamento</th>
                    <th>C</th>
                    <th>Total</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="medicine in medicineData" :key="medicine.Codigo">
                    <td>
                        <!-- <input type="checkbox" :checked="medicine.Reembolso" v-model="medicine.Reembolso"
                            @change="guardarCambios(medicamento)" /> -->
                        <input type="checkbox" :checked="medicine.Reembolso" v-model="medicine.Reembolso"/>
                    </td>
                    <td>{{ medicine.Codigo }}</td>
                    <td>{{ medicine.Medicamento }}</td>
                    <td>{{ medicine.Cantidad }}</td>
                    <td>{{ medicine.Total }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script lang="ts">
import MedicinesDataExample from "../../../../public/JSON/MedicinesExample";
import ControlHeaderTable from "./ControlHeaderTable.vue";

export default {
    components: {
        ControlHeaderTable
    },
    data() {
        return {
            medicineData: MedicinesDataExample
        }
    }
};
</script>