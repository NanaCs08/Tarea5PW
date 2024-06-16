<template>
  <div class="author-details card p-3">
    <div class="header mb-3">
      <h4>Detalle de autor</h4>
    </div>
    <div class="row mb-3">
      <div class="col-md-6 mb-3">
        <div class="info-row">
          <div class="label">Nombre:</div>
          <div class="value">Abraham</div>
        </div>
        <div class="info-row">
          <div class="label">País:</div>
          <div class="value">USA</div>
        </div>
        <div class="info-row">
          <div class="label">Nac:</div>
          <div class="value">1952</div>
        </div>
      </div>
      <div class="col-md-6 mb-3 extra-space">
        <div class="info-row">
          <div class="label">Ocupación:</div>
          <div class="value">Escritor</div>
        </div>
        <div class="info-row">
          <div class="label">Género:</div>
          <div class="value">
            <p class="mb-1">Humor</p>
            <p class="mb-1">Sátira</p>
            <p class="mb-1">Aventuras</p>
          </div>
        </div>
      </div>
    </div>
    <div class="row mb-3">
      <div class="col">
        <div class="table-responsive">
          <DataTable :value="books" responsiveLayout="scroll">
            <Column field="book" header="Libro"></Column>
            <Column field="publisher" header="Editorial"></Column>
            <Column field="year" header="Año"></Column>
            <Column field="edition" header="Edic"></Column>
          </DataTable>
        </div>
      </div>
    </div>
    <div class="row text-end">
      <div class="col">
        <Button label="Cancel" class="p-button-outlined mb-3 mt-1 me-2" />
        <Button label="OK" class="p-button-outlined mb-3 mt-1" />
      </div>
    </div>
  </div>
</template>



<script>
import DataTable from 'primevue/datatable';
import Column from 'primevue/column';
import Button from 'primevue/button';

export default {
  components: {
    DataTable,
    Column,
    Button,
  },
  data() {
    return {
      books: [
        { book: 'El príncipe y el', publisher: 'Alfaguara', year: '1995', edition: '5ta' },
        { book: 'Two Sawyer', publisher: 'Penguin', year: '1965', edition: '2da' },
      ],
    };
  },
};
</script>



<style scoped>
.author-details {
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #fff;
}

.header {
  border-bottom: 1px solid #ddd;
  padding-bottom: 10px;
}

.info-row {
  display: flex;
  justify-content: space-between;
  padding: 5px 0;
}

.label {
  font-weight: bold;
}

.value {
  text-align: left;
  flex: 1;
  padding-left: 10px;
  border-bottom: 1px solid #ddd;
}

.table-responsive {
  margin-top: 20px;
}

.extra-space {
  margin-left: 20px; /* Aumenta este valor para más espacio */
}
</style>

