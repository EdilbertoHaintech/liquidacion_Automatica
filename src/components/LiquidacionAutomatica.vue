<template>
    <div class="canvas">
        <!-- Header: Case Buttons Actions and Data about Case, Ticket & Person -->
        <MainHeader></MainHeader>
        <div class="row">
            <div class="col-75p" style="background-color: var(--primary-soft-color);">
                <Viewer></Viewer>
                <button class="send_btn">
                    <img src="assets/Send.svg" alt="Enviar" class="white_filter">
                </button>
            </div>
            <div class="col-25p">
                <BaseActionSideBar></BaseActionSideBar>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import BaseActionSideBar from './Action Side Bar/BaseActionSideBar.vue';
import MainHeader from './MainHeader.vue';
import Viewer from './Viewer.vue';


export default {
    components: {
    MainHeader,
    Viewer,
    BaseActionSideBar
},
};
</script>

<style>
.canvas {
    width: 96%;
    margin: 3vh auto;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 0px 7px 1px rgba(0, 0, 0, 0.25);
}

.col-75p {
    flex: 0 0 75%;
    max-width: 75%;
    max-height: 80vh;
}

.col-25p {
    flex: 0 0 25%;
    max-width: 25%;
    height: 80vh;
}

.send_btn {
    background-color: var(--secondary-color);
    box-shadow: 0px 0px 7px 1px rgba(0, 0, 0, 0.25);
    border-radius: 25px;
    padding: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    bottom: 0;
    left: 2vw;
}

.send_btn img {
    height: 25px;
}
</style>