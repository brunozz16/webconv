<template>
    <div class="card_conv">
      <div class="state_conv" :style="{ backgroundColor: stateColor }"></div>
      <h3>{{ convenioTitle }}</h3>
      <p>{{ convenioContent }}</p>
      <ConvenioButton />
    </div>
  </template>
  
<script setup>
import ConvenioButton from "./ConvenioButton.vue";
</script>
  <script >
  
  
  const stateOptions = { // Defined in script setup
    prendido: "green",
    apagado: "red"
  };

  export default {
    name: "ConvenioCard",
    props: {
      convenioTitle: {
        type: String,
        default: "vacio"
      },
      convenioContent: {
        type: String,
        default: "vacio"
      },
      state: { // Prop name is "state"
        type: String,
        default: "prendido" // Default state is "prendido"
      }
    },
    computed: {
      stateColor() {
        return stateOptions[this.state] || "black"; // Fallback to black
      }
    }
  };
  </script>
  
<style scoped>
.card_conv {
    
  background-image: linear-gradient(to right, rgb(255, 238, 0), rgb(192, 16, 154));
  background-color: #212F3C;
    padding: 10px;
    
    color: aliceblue;
    border-radius: 10px;
    border: 1px solid black;
    margin: 15px;
    font: inter 90% cursive;
}

.card_conv:hover {
    background-color: rgb(167, 167, 167);
    color: #212F3C;
}

.state_conv{
    width: 100%;
    height: 4px;
    background-color: black;
}
</style>