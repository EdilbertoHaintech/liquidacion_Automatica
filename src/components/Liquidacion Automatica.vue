<template>
    <div class="canvas">
        <!-- Header: Case Buttons Actions and Data about Case, Ticket & Person -->
        <MainHeader></MainHeader>
        <div class="viewer">

        </div>
    </div>
</template>

<script lang="ts">
import MainHeader from './MainHeader.vue';

export default {
    components: {
        MainHeader,
    },
};
</script>

<style>
.canvas {
    width: 95%;
    margin: 3vh auto;
    padding: 10px;
    border-radius: 10px;
    box-shadow: 0px 0px 7px 1px rgba(0, 0, 0, 0.25);
    height: 3000px;
}
</style>