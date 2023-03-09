<template>
    <div class="row pt-1 pb-1 w-95 justify-content-between">
        <!-- Could be replace to a button -->
        <a href="#" class="d-flex align-items-center justify-content-start">
            <img src="../assets/Back_Arrow_Orange.png" alt="Regresar">
            <span class="ml-2">Volver</span>
        </a>
        <div class="col-86p d-flex justify-content-start">
            <div class="back_data">
                <span class="no_validated_text">Ticket #12345</span>
                <span>Tipo<span class="bold">Medicamento</span></span>
                <span>Ingreso<span class="bold">22/02/2023</span></span>
                <span>Plazo Entrega<span class="bold">12/03/2023</span></span>
                <span>Asegurado<span class="bold">Ricardo Darin</span></span>
                <span>RUT<span class="bold">101023345</span></span>
                <span>Farmacia<span class="bold">Nuevo Chile</span></span>
                <span>RUT F<span class="bold">10012345</span></span>
            </div>
        </div>
        <div class="pr-0 d-flex align-items-center">
            <!-- Could be replace to a button -->
            <a href="#" class="d-flex align-items-center justify-content-start">
                <img src="../assets/Prev_Page_Orange.png" alt="Caso Anterior">
            </a>
            <span class="ml-2 mr-2" style="color: var(--primary-color); font-weight: 500;">Casos</span>
            <a href="#" class="d-flex align-items-center justify-content-start">
                <img src="../assets/Next_Page_Orange.png" alt="Caso Siguiente">
            </a>
        </div>
    </div>
</template>

<style>
.back_data {
    padding: 0 !important;
    display: flex;
    align-items: center;
    overflow: auto;
    /* Only One Line */
    white-space: nowrap;
}

.back_data span {
    margin: 0 5px;
}

.col-86p {
    flex: 0 0 86%;
    max-width: 86%;

}
</style>