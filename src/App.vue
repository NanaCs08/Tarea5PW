<template>
  <div class="container border rounded p-3">
    <div class="row border-bottom mb-3 justify-content-center">
      <div class="col-12 text-center">
        <h2>Sistema de Biblioteca</h2>
      </div>
    </div>
    <div class="row justify-content-center">
      <!-- Columna del acordeón -->
      <div class="col-md-3">
        <Accordion :activeIndex="0">
          <AccordionTab header="Autores">
            <div class="accordion-content">
              <Button label="Nuevo" class="p-button-outlined mb-3 mx-2" />
              <Button label="Borrar" class="p-button-outlined mb-3" />
              <div class="scrollable-content border rounded p-2">
                <p>Abraham Silberschatz</p>
                <p>Andrew S. Tanenbaum</p>
              </div>
            </div>
          </AccordionTab>
          <AccordionTab header="Libros">
            <div class="accordion-content">
              <Button label="Nuevo" class="p-button-outlined mb-3 mx-2" />
              <Button label="Borrar" class="p-button-outlined mb-3" />
              <div class="scrollable-content border rounded p-2">
                <p>Operating System Concepts</p>
                <p>Database System Concepts</p>
                <p>Computer Networks</p>
                <p>Modern Operating Systems</p>
              </div>
            </div>
          </AccordionTab>
          <AccordionTab header="Editoriales">
            <div class="accordion-content">
              <Button label="Nuevo" class="p-button-outlined mb-3 mx-2" />
              <Button label="Borrar" class="p-button-outlined mb-3" />
              <div class="scrollable-content border rounded p-2">
                <p>John Wiley & Sons</p>
                <p>Pearson Education</p>
              </div>
            </div>
          </AccordionTab>
          <AccordionTab header="Clasificación">
            <div class="accordion-content">
              <Button label="Nuevo" class="p-button-outlined mb-3 mx-2" />
              <Button label="Borrar" class="p-button-outlined mb-3" />
              <div class="scrollable-content border rounded p-2">
                <p>John Wiley & Sons</p>
                <p>Pearson Education</p>
              </div>
            </div>
          </AccordionTab>
        </Accordion>
      </div>
      <!-- Columna del contenido dinámico -->
      <div class="col-md-8">
        <TabView>
          <TabPanel header="Autor">
            <AutorComponent />
          </TabPanel>
          <TabPanel header="Libro">
            <LibroComponent />
          </TabPanel>
          <TabPanel header="Editorial">
            <EditorialComponent />
          </TabPanel>
        </TabView>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import Accordion from 'primevue/accordion';
import AccordionTab from 'primevue/accordiontab';
import Button from 'primevue/button';
import TabView from 'primevue/tabview';
import TabPanel from 'primevue/tabpanel';

import AutorComponent from './components/AutorComponent.vue';
import LibroComponent from './components/LibroComponent.vue';
import EditorialComponent from './components/EditorialComponent.vue';

export default {
  components: {
    Accordion,
    AccordionTab,
    Button,
    TabView,
    TabPanel,
    AutorComponent,
    LibroComponent,
    EditorialComponent
  },
  setup() {
    const currentComponent = ref('AutorComponent');
    return { currentComponent };
  }
};
</script>

<style scoped>
.container {
  background-color: #f8f9fa;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  max-width: 1200px; /* Limitar el ancho máximo del contenedor */
  margin: auto; /* Centrar horizontalmente */
}

.row {
  display: flex;
}

h2 {
  font-family: 'Arial', sans-serif;
  color: #007bff;
}

.accordion-button::after {
  display: none;
}

.accordion-content {
  padding: 10px;
  background-color: #fff;
  border-radius: 5px;
}

.scrollable-content {
  height: 200px;
  overflow-y: scroll;
  background-color: #f1f1f1;
  padding: 10px;
}

.scrollable-content p {
  margin: 0;
  padding: 5px 0;
}

.accordion-button:not(.collapsed),
.accordion-button:not(.collapsed):active,
.accordion-button:not(.collapsed):focus {
  background-color: inherit !important;
  color: inherit !important;
}

.tabview {
  background-color: #fff;
  border-radius: 5px;
  padding: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.tabview .p-tabview-nav {
  border-bottom: 1px solid #dee2e6;
}

.tabview .p-tabview-nav .p-tabview-nav-link {
  padding: 0.5rem 1rem;
}

.tabview .p-tabview-nav .p-tabview-nav-link.active {
  background-color: #007bff;
  color: #fff;
}
</style>
