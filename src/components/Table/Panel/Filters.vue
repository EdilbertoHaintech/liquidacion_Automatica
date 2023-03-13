<template>
    <div>
        <h3>Filtros</h3>
        <CustomSelectList :items="filters" />
        <button type="button" class="primary br-a-5 mt-4" :disabled="canCleanFilters">
            <img src="assets/Undo_Arrow1.svg" alt="Limipiar Filtro" class="white_filter"> Limpiar filtros
        </button>
    </div>
</template>

<script>
import CustomSelectList from '../../CustomSelect/List.vue';
import sampleTable from '../../../../public/JSON/sample-table';

export default {
    components: {
        CustomSelectList,
    },
    data() { 
        return {
            filters: sampleTable,
            canCleanFilters: true
        }
    }
}
</script>

<style scoped>
button[type="button"] {
    color: white;
    padding: 4px 20px;
    width: 90%
    /* background-color: var(--primary-color); */
}
</style>