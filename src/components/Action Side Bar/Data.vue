<template>
    <div class="d-flex flex-column">
        <span class="title_section">Datos</span>
        <div class="data" v-for="ticket in tickets" :key="ticket.Ticket">
            <span :class="{ 'validated_text': ticket.Validado == true, 'no_validated_text': ticket.Validado != true }">Ticket #{{ ticket.Ticket }}</span>
            <div>
                <span>Tipo</span><span class="bold">{{ ticket.Tipo }}</span>
            </div>
            <div>
                <span>Validado</span><span class="bold">{{ ticket.Validado }}</span>
            </div>
            <div>
                <span>Ingreso</span><span class="bold">{{ ticket.Ingreso }}</span>
            </div>
            <div>
                <span>Plazo Entrega</span><span class="bold">{{ ticket.PlazoEntrega }}</span>
            </div>
            <div>
                <span>Asegurado</span><span class="bold">{{ ticket.Asegurado }}</span>
            </div>
            <div>
                <span>RUT</span><span class="bold">{{ ticket.RUT }}</span>
            </div>
            <div>
                <span>Farmacia</span><span class="bold">{{ ticket.Farmacia }}</span>
            </div>
            <div>
                <span>RUT F</span><span class="bold">{{ ticket.RUTfarmacia }}</span>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import SingleTicket from "../../../public/JSON/SingleTicket";

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

.data div {
    width: 100%;
    display: flex!important;
    justify-content: space-between;
}
</style>