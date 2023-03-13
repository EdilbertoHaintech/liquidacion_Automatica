<template>
    <CustomSelectItem class="mb-2" v-for="(item, index) of items" :key="index" v-bind="item" />
</template>

<script lang="ts">
import CustomSelectItem from './Item.vue'
export default {
    props: {
        items: {
            type: Array,
            default: []
        }
    },
    components: {
        CustomSelectItem  
    },
}
</script>