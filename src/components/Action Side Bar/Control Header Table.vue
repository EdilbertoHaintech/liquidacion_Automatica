<template>
    <div class="control_header d-flex gap-10 justify-space-between align-center flex-wrap text-unselectable">
        <div class="search">
            <button type="button" class="icon">
                <label for="search">
                    <img src="assets/Search.svg" alt="Buscador" class="mr-2 white_filter">
                </label>
            </button>
            <input type="text" id="search" placeholder="Buscar">
        </div>
        <div class="actions-section d-flex gap-10">
            <button type="button" class="icon">
                <img src="assets/Add.svg" alt="Agregar" class="mr-2 white_filter">
            </button>
            <button type="button" class="icon">
                <img src="assets/Edit.svg" alt="Editar" class="mr-2 white_filter">
            </button>
            <button type="button" class="icon">
                <img src="assets/Delete.svg" alt="Eliminar" class="mr-2 white_filter">
            </button>
        </div>
    </div>
</template>

<style>
.control_header {
    background-color: var(--primary-color);
    border-radius: 5px 5px 0 0;
}

input {
    border: none;
    border-bottom: 2px solid white;
    color: #fff;
}

input::placeholder {
    color: #fff;
}
</style>