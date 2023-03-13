<template>
    <CustomCheckboxItem v-for="(item, index) of items" :key="index" v-bind="item" />
</template>

<script lang="ts">
import CustomCheckboxItem from './Item.vue';

export default {
    components: {
        CustomCheckboxItem
    },
    props: {
        items: {
            type: Array,
            default: []
        }
    }
}
</script>