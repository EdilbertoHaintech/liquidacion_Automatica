<template>
    <div class="table_header d-flex justify-content-between align-content-center">
        <div class="title">
            <button type="button" class="icon">
                <img src="assets/Filter.svg" alt="Filtrar" class="mr-2">
            </button>
            <span>Filtros - Campos</span> 
        </div>
        <div class="search">
            <button type="button" class="icon">
                <label for="search">
                    <img src="assets/Search.svg" alt="Buscador" class="mr-2">
                </label>
            </button>
            <input type="text" id="search" placeholder="Buscar">
        </div>
        <div class="pagination d-flex">
            <label for="elements" class="mr-8">Elementos</label>
            <select name="elements" id="elements">
                <option value="50" selected>50</option>
            </select>
        </div>
        <div class="actions-section d-flex gap-10">
            <button type="button" class="icon">
                <img src="assets/Prev_Page.svg" alt="Pagina previa" class="mr-2">
            </button>
            <button type="button" class="icon">
                <img src="assets/Prev_Arrow.svg" alt="Previo"  class="mr-2">
            </button>
            <button type="button" class="icon">
                <img src="assets/Prev_Arrow.svg" alt="Siguiente" style="transform: rotate(180deg)"  class="mr-2">
            </button>
            <button type="button" class="icon">
                <img src="assets/Prev_Page.svg" alt="Pagina siguiente" style="transform: rotate(180deg)"  class="mr-2">
            </button>
        </div>
        <div class="selected-items">
            Seleccionados <strong>12</strong>
        </div>
        <div class="actions-section d-flex gap-10">
            <button type="button" class="icon">
                <img src="assets/Add.svg" alt="Buscador" class="mr-2">
            </button>
            <button type="button" class="icon">
                <img src="assets/Edit.svg" alt="Editar" class="mr-2"> 
            </button>
            <button type="button" class="icon">
                <img src="assets/Delete.svg" alt="Eliminar" class="mr-2"> 
            </button>
        </div>
    </div>
</template>