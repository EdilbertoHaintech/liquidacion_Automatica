<template>
    <div class="canvas">
        <!-- Header: Case Buttons Actions and Data about Case, Ticket & Person -->
        <MainHeader></MainHeader>
        <!-- Content -->
        <div class="row">
            <div class="col-75p" style="background-color: var(--primary-soft-color);">
                <InnerViewer></InnerViewer>
                <!-- <Viewer2></Viewer2> -->
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
import Viewer2 from './Viewer2.vue';

export default {
    components: {
    InnerViewer,
    BaseActionSideBar,
    MainHeader,
    Viewer2
},
};
</script>

<style>
.col-75p {
    flex: 0 0 75%;
    max-width: 75%;
    height: 700px;
    position: relative;
}

.col-25p {
    flex: 0 0 25%;
    max-width: 25%;
}

.send_btn {
    background-color: var(--secondary-color);
    box-shadow: 0px 0px 7px 1px rgba(0, 0, 0, 0.25);
    border-radius: 25px;
    padding: 12px;
    margin: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    bottom: 0;
    left: 0;
}

.send_btn img {
    height: 25px;
}
</style>