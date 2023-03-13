<template>
    <div class="d-flex">
        <div class="col-2 d-flex- flex-column table-sidebar">
            <DynamicTableFilters />
            <DynamicTableFields />
        </div>
        <div class="col-10">
            <TablePreHeader />
            <Table></Table>
        </div>
    </div>
</template>

<script lang="ts">
import DynamicTableFilters from './Panel/Filters.vue';
import DynamicTableFields from './Panel/Fields.vue';
import TablePreHeader from './TablePreHeader.vue'
import Table from './Table.vue';

export default {
    components: {
        DynamicTableFilters,
        DynamicTableFields,
        Table,
        TablePreHeader
    }
}
</script>

<style>
.table-sidebar{
    max-height: 90vh;
    overflow-y: auto;
}
</style>