<template>
  <div class="tab-pane fade" id="editorial-tab">
    <h2>Detalle de editorial</h2>
    <div class="row">
      <!-- Columna izquierda -->
      <div class="col-md-6">
        <div class="card">
          <div class="card-header">
            Información General
          </div>
          <div class="card-body">
            <table class="table table-borderless">
              <tbody>
                <tr>
                  <td><strong>Nombre:</strong></td>
                  <td>John Wiley e hijos</td>
                </tr>
                <tr>
                  <td><strong>País:</strong></td>
                  <td>
                    <div class="scroll">
                      Estados Unidos
                    </div>
                  </td>
                </tr>
                <tr>
                  <td><strong>Fundado:</strong></td>
                  <td>1807</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
      <!-- Columna derecha -->
      <div class="col-md-6">
        <div class="card">
          <div class="card-header">
            Detalles Específicos
          </div>
          <div class="card-body">
            <table class="table table-borderless">
              <tbody>
                <tr>
                  <td><strong>Género:</strong></td>
                  <td>Académico</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
    <!-- Tabla de libros -->
    <div class="row mt-3">
      <div class="col">
        <div class="card">
          <div class="card-header bg-primary text-white">
            Listado de Libros
          </div>
          <div class="card-body">
            <table class="table table-bordered table-hover">
              <thead class="table-primary">
                <tr>
                  <th scope="col">Título del Libro</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="book in books" :key="book.id">
                  <td>{{ book.book }}</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
    <!-- Botones de acción -->
    <div class="row mt-3">
      <div class="col text-end">
        <button type="button" class="btn btn-success">Guardar cambios</button>
        <button type="button" class="btn btn-danger ms-2">Eliminar</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      books: [
        { id: 1, book: 'Conceptos del sistema operativo' },
        { id: 2, book: 'Conceptos del sistema de base de datos' }
      ]
    };
  }
};
</script>

<style scoped>
.scroll {
  max-height: 100px; /* Altura máxima para el scroll */
  overflow-y: auto; /* Añadir scroll vertical si es necesario */
}

.card {
  margin-bottom: 20px; /* Espacio entre tarjetas */
}
</style>
