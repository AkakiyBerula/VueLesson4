<template>
  <div>
    <div class="row">
      <div class="col">
        <label for="rows">Кількість рядків:</label>
        <input type="number" class="form-control" id="rows" min="0" max="12" v-model="rowCount">
      </div>
      <div class="col">
        <label for="columns">Кількість стовпців:</label>
        <input type="number" class="form-control" id="columns" min="0" max="12" v-model="columnCount"> 
      </div>
    </div>

    <v-simple-table>
        <thead>
          <tr>
            <th v-for="n in columnCount" :key="n">Row {{ n }}</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="i in rowCount" :key="i">
            <td v-for="j in columnCount" :key="j" class="info">row {{ i }}, col {{ j }}</td>
          </tr>
        </tbody>
    </v-simple-table>
  </div>
</template>

<script>
export default {
  name: "FlexTable",
  data() {
    return {
      rowCount: 3,
      columnCount: 3
    };
  }
}
</script>

<style>
table {
  border-collapse: collapse;
}

td {
  border: 1px solid black;
  padding: 8px;
}

.info {
  background-color: #e1f5fe;
}
</style>



