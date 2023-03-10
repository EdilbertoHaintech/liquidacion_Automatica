<template>
    <div class="d-flex flex-column">
        <span class="title_section">Validación</span>
        <div class="row mb-3">
            <img src="assets/Check_Green.svg" alt="Validado">
            <span class="text_after_icon">Validación Boleta</span>
        </div>
        <div class="row mb-3">
            <img src="assets/Check_Green.svg" alt="Validado">
            <span class="text_after_icon">Validación Doctor</span>
        </div>
        <div class="d-flex justify-content-center">
            <div class="final_message">
                <img src="assets/Check_Green.svg" alt="Validado">
                <span class="text_after_icon">Validación Completa</span>
            </div>
        </div>
    </div>
</template>

<style>
.final_message {
    display: flex;
    align-content: center;
    position: absolute;
    bottom: 4vh;
}
</style>