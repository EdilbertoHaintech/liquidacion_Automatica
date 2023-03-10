<template>
    <div class="d-flex flex-column">
        <span class="title_section">Medicamentos</span>
        <ControlHeaderTable></ControlHeaderTable>
        <!-- Generic Table -->
        <table>
            <thead>
                <tr>
                    <th>Reembolso</th>
                    <th>Código</th>
                    <th>Cantidad</th>
                    <th>Total</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><input type="checkbox"></td>
                    <td>001</td>
                    <td>2</td>
                    <td>$10.00</td>
                </tr>
                <tr>
                    <td><input type="checkbox"></td>
                    <td>002</td>
                    <td>1</td>
                    <td>$5.00</td>
                </tr>
                <tr>
                    <td><input type="checkbox"></td>
                    <td>003</td>
                    <td>3</td>
                    <td>$15.00</td>
                </tr>
            </tbody>
        </table>

    </div>
</template>

<script lang="ts">
import ControlHeaderTable from './Control Header Table.vue';

export default {
    components: {
        ControlHeaderTable
    },
};
</script>