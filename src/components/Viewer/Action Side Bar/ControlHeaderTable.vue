<template>
    <div class="control_header d-flex justify-content-between align-content-center">
        <div class="search row">
            <button type="button">
                <img src="assets/Search.svg" alt="Buscador" class="white_filter">
            </button>
            <input type="text" id="search" placeholder="Buscar">
        </div>
        <div class="actions-section row">
            <button type="button">
                <img src="assets/Add.svg" alt="Agregar" class="white_filter">
            </button>
            <button type="button">
                <img src="assets/Edit.svg" alt="Editar" class="white_filter">
            </button>
            <button type="button">
                <img src="assets/Delete.svg" alt="Eliminar" class="white_filter">
            </button>
        </div>
    </div>
</template>

<style>
.control_header {
    background-color: var(--primary-color);
    border-radius: 5px 5px 0 0;
    padding: 10px;
}

input {
    border: none;
    border-bottom: 2px solid white;
    color: #fff;
    max-width: 10vw;
}

input::placeholder {
    color: #fff;
}

button img {
    display: flex;
}
</style>