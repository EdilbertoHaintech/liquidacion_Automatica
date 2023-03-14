<template>
    <div class="canvasValidation">
        <span class="title_section">Validación</span>
        <details>
            <summary class="checkGreen">Validación Boleta</summary>
            <ul>
                <li class="checkGreen">
                    <span class="text_after_icon">RUT</span>
                </li>
                <li class="checkGreen">
                    <span class="text_after_icon">Folio</span>
                </li>
                <li>
                    <img src="assets/Sii.svg" class="ss" alt="Captura Validación Servicio Impuestos Internos">
                </li>
            </ul>
        </details>
        <details>
            <summary class="cancelRed">Validación Doctor</summary>
            <ul>
                <li class="cancelRed">
                    <span class="text_after_icon">RUT</span>
                </li>
                <li class="cancelRed">
                    <span class="text_after_icon">Nombre Médico</span>
                </li>
                <li>
                    <img src="assets/SdS.jpg" class="ss" alt="Captura Validación Superintendencia de Salud">
                </li>
            </ul>
        </details>
        <div class="d-flex justify-content-center">
            <div class="final_message">
                <img src="assets/Check_Green.svg" alt="Validado">
                <span class="text_after_icon validated">Validación Completa</span>
            </div>
        </div>
    </div>
</template>

<style scoped>
.canvasValidation {
    display: flex;
    flex-direction: column;
    overflow: auto;
    height: 100%;
}

.checkGreen {
    appearance: none;
    -webkit-appearance: none;
    cursor: pointer;
    background-repeat: no-repeat;
    background-position: left center;
    padding: 5px 0 5px 30px;
    background-image: url('../../../../public/assets/Check_Green.svg');
}


.cancelRed {
    appearance: none;
    -webkit-appearance: none;
    cursor: pointer;
    background-repeat: no-repeat;
    background-position: left center;
    padding: 5px 0 5px 30px;
    background-image: url('../../../../public/assets/Cancel.svg');
}

.ss {
    height: 200px;
    width: 100%;
}

/* Dont show triangle before text */
details>summary {
    list-style: none;
}

details>summary::-webkit-details-marker {
    display: none;
}

.final_message {
    display: flex;
    align-content: center;
    margin: 5vh 0 0 0;
}

.final_message .validated {
    color: var(--green-validated-color);
}

.final_message .noValidated {
    color: var(--red-no-validated-color);
}
</style>