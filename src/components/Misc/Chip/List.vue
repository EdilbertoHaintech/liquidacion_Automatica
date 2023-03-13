<template>
    <span class="chip-list">
        <ChipItem v-for="(item, index) in items" :key="index" v-bind="item" />
    </span>
</template>

<script lang="ts">
import ChipItem from './Item.vue';

export default {
    components: {
        ChipItem
    },
    props: {
        items: {
            type: Array,
            default: []
        }
    }
}
</script>