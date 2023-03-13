<template>
    <div class="row pt-0 pb-3 justify-content-between">
        <!-- Could be replace to a button -->
        <a href="#" class="d-flex align-items-center justify-content-start">
            <img src="assets/Prev_Arrow.svg" alt="Regresar" class="primary_color_filter">
            <span class="text_after_icon">Volver</span>
        </a>
        <div class="col-86p d-flex justify-content-start">
            <div class="back_data" v-for="ticket in tickets" :key="ticket.Ticket">
                <span :class="{ 'validated_text': ticket.Validado == true,
                    'no_validated_text': ticket.Validado != true }">Ticket#{{ ticket.Ticket }}</span>
                <span>Tipo</span><span class="bold">{{ ticket.Tipo }}</span>
                <!-- <span>Validado</span><span class="bold">{{ ticket.Validado }}</span> -->
                <span>Ingreso</span><span class="bold">{{ ticket.Ingreso }}</span>
                <span>Plazo Entrega</span><span class="bold">{{ ticket.PlazoEntrega }}</span>
                <span>Asegurado</span><span class="bold">{{ ticket.Asegurado }}</span>
                <span>RUT</span><span class="bold">{{ ticket.RUT }}</span>
                <span>Farmacia</span><span class="bold">{{ ticket.Farmacia }}</span>
                <span>RUT F</span><span class="bold">{{ ticket.RUTfarmacia }}</span>
            </div>
        </div>
        <div class="pr-0 d-flex align-items-center">
            <!-- Could be replace to a button -->
            <a href="#" class="d-flex align-items-center justify-content-start">
                <img src="assets/Prev_Arrow.svg" alt="Caso Anterior" class="primary_color_filter">
            </a>
            <span class="ml-2 mr-2" style="color: var(--primary-color); font-weight: 500;">Casos</span>
            <a href="#" class="d-flex align-items-center justify-content-start">
                <img src="assets/Next_Arrow.svg" alt="Caso Siguiente" class="primary_color_filter">
            </a>
        </div>
    </div>
</template>

<script lang="ts">
import SingleTicket from "../../public/JSON/SingleTicket";

export default {
    components: {
    },
    data() {
        return {
            tickets: SingleTicket
        }
    }
};
</script>

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