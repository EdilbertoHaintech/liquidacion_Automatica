<template>
    <div class="d-flex justify-content-between" style="padding: 1vh 3vw 1vh 0;">
        <div>
            Filtros aplicados
            <ChipList class="ml-4" :items="appliedFilters" />
        </div>
        <div>
            Total Registros <strong>3850</strong>
        </div>
    </div>
</template>

<script lang="ts">
import ChipList from '../Misc/Chip/List.vue';

export default {
    components: {
        ChipList
    },
    data() {
        return {
            appliedFilters: [
                {
                    text: 'Alekos',
                    canRemove: true
                }
            ]
        }
    }
}
</script>