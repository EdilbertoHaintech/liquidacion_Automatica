<template>
    <div class="d-flex flex-column">
        <span class="title_section">Medicamentos</span>
        <ControlHeaderTable></ControlHeaderTable>
        <!-- Generic Table -->
        <!-- <table>
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
        </table> -->

        <ul>
            <li v-for="user in data1.usuarios" :key="user.id">
                {{ user.nombre }} {{ user.apellido }}
            </li>
        </ul>
        <table>
            <thead>
                <tr>
                    <th>Nombre</th>
                    <th>Apellido</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="user in data2" :key="user.id">
                    <td>{{ user.nombre }}</td>
                    <td>{{ user.apellido }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script lang="ts">
import ControlHeaderTable from './Control Header Table.vue';
import SimpleExample from "../../../public/JSON/Simple Example";
import SimpleExample1 from "../../../public/JSON/Simple Example - Copy";

export default {
    components: {
        ControlHeaderTable
    },
    data() {
        return {
            data1: SimpleExample,
            data2: SimpleExample1
        }
    }
};
</script>