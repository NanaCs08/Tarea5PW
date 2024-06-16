<template>
  <div class="book-details card p-4">
    <div class="row mb-3">
      <div class="col">
        <h4>Detalle de libros</h4>
      </div>
    </div>
    <div class="row mb-4">
      <div class="col-3 text-end">
        <p class="mb-3">Nombre:</p>
        <p class="mb-3">ISBN:</p>
      </div>
      <div class="col-9">
        <p class="form-control mb-3">Las aventuras de Tom Sawyer</p>
        <p class="form-control mb-3">12244-5678-45</p>
      </div>
    </div>
    <div class="row mb-4">
      <div class="col-6">
        <p>Año:</p>
        <div class="scrollable-content">
          <p class="form-control mb-0">5th</p>
        </div>
      </div>
      <div class="col-6">
        <p>Edición:</p>
        <div class="scrollable-content">
          <p class="form-control mb-0">5</p>
        </div>
      </div>
    </div>
    <div class="row align-items-center mb-4">
      <div class="col">
        <p class="d-inline-block mb-0">Año:</p>
        <a href="#" class="ms-3 text-primary">Ediciones Algaguara</a>
        <Button label="Cambiar Editorial" class="p-button-outlined ms-3" />
      </div>
    </div>
    <div class="row mb-4" style="border-bottom: 1px solid black;">
      <div class="col-3 text-end">
        <p>Autores:</p>
      </div>
      <div class="col-6">
        <div class="scrollable-content">
          <p class="form-control mb-0">Mark Twain</p>
        </div>
      </div>
      <div class="col-3 text-end">
        <Button label="Agregar" class="p-button-outlined mb-2" />
        <Button label="Eliminar" class="p-button-outlined mb-2" />
      </div>
    </div>
    <div class="row text-end">
      <div class="col">
        <Button label="Cancel" class="p-button-outlined mb-3 me-2" />
        <Button label="OK" class="p-button mb-3" />
      </div>
    </div>
  </div>
</template>


<script>
import Button from 'primevue/button';

export default {
    components: {
        Button,
    }
};
</script>


<style scoped>
.book-details {
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #fff;
}

.scrollable-content {
  max-height: 80px;
  overflow-y: auto;
}

.mb-3 {
  margin-bottom: 1rem !important;
}

.ms-3 {
  margin-left: 1rem !important;
}

.form-control {
  border: 1px solid #ced4da;
  border-radius: .25rem;
  padding: .375rem .75rem;
  background-color: #fff;
  background-clip: padding-box;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
  color: #495057;
}
</style>
