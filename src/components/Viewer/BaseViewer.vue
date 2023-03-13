<template>
    <div class="canvas">
        <!-- Header: Case Buttons Actions and Data about Case, Ticket & Person -->
        <MainHeader></MainHeader>
        <!-- Content -->
        <div class="row">
            <div class="col-75p" style="background-color: var(--primary-soft-color);">
                <InnerViewer></InnerViewer>
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
import InnerViewer from './InnerViewer.vue';
import MainHeader from './MainHeader.vue';


export default {
    components: {
    InnerViewer,
    BaseActionSideBar,
    MainHeader
},
};
</script>

<style>
.col-75p {
    flex: 0 0 75%;
    max-width: 75%;
    max-height: 80vh;
}

.col-25p {
    flex: 0 0 25%;
    max-width: 25%;
    max-height: 80vh;
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