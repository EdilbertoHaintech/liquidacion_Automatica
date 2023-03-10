<template>
    <div class="d-flex flex-column">
        <span class="title_section">Medicamentos</span>
        <ControlHeaderTable></ControlHeaderTable>
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