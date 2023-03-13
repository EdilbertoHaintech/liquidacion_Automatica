<template>
  <div class="tabla ma-8">
    <table v-if="headers.length" class="claims-table">
      <thead>
        <tr>
          <th>
            <!-- Checkbox Column, en lugar de ngfor* se usa v-for -->
            <input type="checkbox" />
          </th>
          <template v-for="column in headers" :key="column.code">
            <th>{{ column.name }}</th>
          </template>
        </tr>
      </thead>
      <tbody>
        <!-- mouseover-mouseleave esta propiedades exclusivas de Vue nos permiten hacer el hoover de los botones-->
        <tr v-for="(item, index) in items" :key="index" :id="'row-' + item.id" @mouseover="hoveredRow = index"
          @mouseleave="hoveredRow = null">
          <td>
            <input type="checkbox" v-model="selection" :value="item.id" />
          </td>
          <template v-for="column in headers" :key="column.code">
            <td>
              {{ item[column.code] }}
            </td>
          </template>
          <td v-if="index === hoveredRow">
            <div>
              <button @click="onClickButtonEdit(item)"><img src="assets/Edit.svg" alt="Editar" class="mr-2"> </button>
              <button @click="onClickButtonDelete(item)"><img src="assets/Delete.svg" alt="Eliminar" class="mr-2">
              </button>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>


<script>
import sampleTable from '../../../public/JSON/sample-table';
import sampleData from '../../../public/JSON/sample-data';
export default {
  data() {
    return {
      headers: sampleTable,
      items: sampleData,
      hoveredRow: null //No se esta pasando el Mouse, por lo tanto no muestra nada
    }
  },

  methods: {
    onClickButtonEdit(item) {
      // Lógica para el botón de editar
    },
    onClickButtonImport(item) {
      // Lógica para el botón de importar
    },
    onClickButtonDelete(item) {
      // Lógica para el botón de borrar
    },
    onClickButtonCampaign(item) {
      // Lógica para el botón de Campana
    }
  }
}
</script>


<style>
.tabla {
  max-height: 80vh;
  max-width: 100%;
  overflow-y: auto;
  overflow-x: auto;
}

table {
  width: 100%;
  border-collapse: collapse;
  background-color: white;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
}

th,
td {
  text-transform: capitalize;
  text-align: left;
  border-bottom: 1px solid #ddd;
}

th {
  background-color: var(--primary-soft-color);
}

tbody tr:nth-of-type(even) {
  background-color: #f3f3f3;
}

tbody tr:hover {
  background-color: #ddd;
}

td input[type=checkbox] {
  margin-right: 10px;
}

td button {
  margin-right: 5px;
}
</style>
