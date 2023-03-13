<template>
    <h2>{{ title }}</h2>
    <!-- <div class="d-flex flex-column table-container">
        <DynamicTablePrimaryHeader />
        <DynamicTablePrimaryContent />
    </div> -->
    <div class="canvas" style="padding: 0;">
        <DynamicTablePrimaryHeader />
        <!-- <DynamicTablePrimaryContent /> -->
    </div>
</template>

<script lang="ts">
import DynamicTablePrimaryHeader from './PrimaryHeader.vue';
// import DynamicTablePrimaryContent from './PrimaryContent.vue';

export default {
    data() {
        return {
            title: 'Auditoria'
        }
    },
    components: {
        DynamicTablePrimaryHeader,
        // DynamicTablePrimaryContent
    },
};
</script>

<style>
h2 {
    width: 96%;
    margin: 2vh auto;
    font-size: 16px;
    font-weight: 600;
}
</style>
