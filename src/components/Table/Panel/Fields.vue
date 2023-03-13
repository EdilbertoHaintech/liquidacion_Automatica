<template>
    <div>
        <h3>Columnas tabla</h3>
        <CustomCheckboxList :items="checkboxs" />
    </div>
</template>

<script>
import CustomCheckboxList from '../../CustomCheckbox/List.vue';
import sampleTable from '../../../../public/JSON/sample-table';

export default {
    components: {
        CustomCheckboxList
    },
    data () {
        return {
            checkboxs: sampleTable
        }
    }
}
</script>