<template>
    <div class="bigdiv">
      <h1>Lista de Convenios</h1>
      <ul>
          <li v-for="convenio in convenios" :key="convenio.id">
        <ConvenioCard :convenioTitle="convenio.nombre" :convenioContent="convenio.descripcion"/>
      </li>
        
      </ul>
    </div>
</template>
  
<script>
//import ConvenioCard from "./ConvenioCard.vue";
import axios from 'axios';

export default {
  data() {
    return {
      convenios: []
    };
  },
  mounted() {
    this.fetchConvenios();
  },
  methods: {
    fetchConvenios() {
      axios.get('http://localhost:3000/convenios')
        .then(response => {
          this.convenios = response.data;
        })
        .catch(error => {
          console.error("Error fetching convenios:", error);
        });
    }
  }
};
</script>
  
  <style scoped>
  .bigdiv {
    background-color: red;
  }
  /* Estilos para el componente */
  </style>
  