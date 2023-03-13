<template>
    <select :class="$attrs.class" v-if="generateFilter" :name="code" :id="code" :disabled="!generateFilter">
        <option selected>
            {{ name }}
        </option>
        <option v-for="(option, index) of options" :key="index" :value="option.value">{{ option.name }}</option>
    </select>
</template>

<script>
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
    }
}
</script>