<template>
    <span class="custom-chip">
        {{ text }}
        <span class="closebtn is-clickable font-weight-bold" v-if="canRemove">&times;</span>
    </span>
</template>

<script>
export default {
    props: ['text', 'canRemove']
}
</script>

<style>
.custom-chip{
    background: var(--primary-color);
    border-radius: 5px;
    padding: 4px 8px;
    font-size: 12px;
    color: white;
}

.closebtn {
    transition: opacity ease 0.5s;
    font-size: 18px;
    vertical-align: middle;
}

.closebtn:hover {
    opacity: 0.4;
}
</style>