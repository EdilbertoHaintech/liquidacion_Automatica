<template>
    <div class="d-flex flex-column">
        <span class="title_section">Datos</span>
        <div class="data">
            <span class="no_validated_text">Ticket #12345</span>
            <div class="row d-flex">
                <span>Tipo</span><span class="bold">Medicamento</span>
            </div>
            <div class="row">
                <span>Ingreso</span><span class="bold">22/02/2023</span>
            </div>
            <div class="row">
                <span>Plazo Entrega</span><span class="bold">12/03/2023</span>
            </div>
            <div class="row">
                <span>Asegurado</span><span class="bold">Ricardo Darin</span>
            </div>
            <div class="row">
                <span>RUT</span><span class="bold">101023345</span>
            </div>
            <div class="row">
                <span>Farmacia</span><span class="bold">Nuevo Chile</span>
            </div>
            <div class="row">
                <span>RUT F</span><span class="bold">10012345</span>
            </div>
        </div>
    </div>
</template>

<style>
.data {
    padding: 0 !important;
    display: flex;
    align-items: flex-start;
    overflow: auto;
    flex-direction: column;
}

.data span {
    margin: 3px 5px;
}
</style>