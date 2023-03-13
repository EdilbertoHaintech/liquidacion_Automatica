<template>
    <div>
        <input type="checkbox" :name="code" :id="code" :placeholder="name" :checked="display">
        <label for="Nombre">{{ name }}</label>
    </div>
</template>

<script lang="ts">
export default {
    inheritAttrs: false,
    props: {
        name: String,
        code: String,
        display: Boolean,
        generateFilter: Boolean,
        options: {
            type: Array,
            default: []
        }
    },
}
</script>