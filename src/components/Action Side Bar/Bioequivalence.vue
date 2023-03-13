<template>
    <div class="d-flex flex-column">
        <span class="title_section">Bioequivalencia</span>
        <ControlHeaderTable></ControlHeaderTable>
        <details>
            <summary>Paracetamol:</summary>
            <ul>
                <li>Advil</li>
                <li>Dolorin</li>
                <li>Medicamento Equivalente 1</li>
                <li>Medicamento Equivalente 2</li>
            </ul>
        </details>
        <details>
            <summary>Medicamento 1:</summary>
            <ul>
                <li>Medicamento Equivalente 1</li>
                <li>Medicamento Equivalente 2</li>
                <li>Medicamento Equivalente 3</li>
                <li>Medicamento Equivalente 4</li>
            </ul>
        </details>
        <details>
            <summary>Medicamento 2:</summary>
            <ul>
                <li>Medicamento Equivalente 1</li>
                <li>Medicamento Equivalente 2</li>
                <li>Medicamento Equivalente 3</li>
                <li>Medicamento Equivalente 4</li>
            </ul>
        </details>
        <details>
            <summary>Medicamento 3:</summary>
            <ul>
                <li>Medicamento Equivalente 1</li>
                <li>Medicamento Equivalente 2</li>
                <li>Medicamento Equivalente 3</li>
                <li>Medicamento Equivalente 4</li>
            </ul>
        </details>
    </div>
</template>

<script lang="ts">
import ControlHeaderTable from './ControlHeaderTable.vue';



export default {
    components: {
    ControlHeaderTable
},
};
</script>